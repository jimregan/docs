---
layout: base
title:  'Structure'
---

# Syntax: General Principles

The goal is a set of broadly observed "universal dependencies" that work across languages. Such dependencies seek to maximize parallelism by allowing the same grammatical relation to be annotated the same way across languages, while making enough crucial distinctions such that different things can be differentiated.
The goal of parallelism has limits: The standard does not postulate and annotate "empty" things that do not appear in various languages, and it allows the use of language-specific refinements of universal dependencies to represent particular relations of language-particular importance. We now try to lay down some general principles that should guide the use of universal 
dependencies to achieve as much parallelism as possible (but not more) across languages.

## The Primacy of Content Words

Dependency relations hold primarily between content words, rather than being indirect relations mediated by function words.

<div id="s1a" class="sd-parse">
The cat could have chased all the dogs down the street .
nsubj(chased, cat)
dobj(chased, dogs)
nmod(chased, street)
</div>

Function words attach as direct dependents of the most closely related content word.

<div id="s1b" class="sd-parse">
The cat could have chased all the dogs down the street .
det(cat, The)
aux(chased, could)
aux(chased, have)
det(dogs, all)
det(dogs, the-7)
case(street, down)
det(street, the-10)
</div>

Punctuation attaches to the head of the clause or phrase to which they belong.

<div id="s1c" class="sd-parse">
The cat could have chased all the dogs down the street .
punct(chased, .)
</div>

Putting this together gives a complete dependency tree where internal nodes
are content words and where function words and punctuation appear as leaves.

<div id="s1" class="sd-parse">
The cat could have chased all the dogs down the street .
nsubj(chased, cat)
dobj(chased, dogs)
nmod(chased, street)
det(cat, The)
aux(chased, could)
aux(chased, have)
det(dogs, all)
det(dogs, the-7)
case(street, down)
det(street, the-10)
punct(chased, .)
</div>

Preferring content words as heads maximizes parallelism between languages because content words vary less than function words between languages. In particular, one commonly finds the same grammatical relation being expressed by morphology in some languages or constructions and by function words in other languages or constructions, while some languages may not mark the information at all (such as not marking tense or definiteness).

<div id="s2a" class="sd-parse">
On a dormi ...
nsubj(dormi, On)
aux(dormi, a)
</div>

<div id="s2b" class="sd-parse">
We slept ...
nsubj(slept, We)
</div>

## The Status of Function Words

The primacy of content words implies that function words normally do not have dependents of their own. 
In particular, it means that multiple function words related to the same content word always appear as 
siblings, never in a nested structure, regardless of whether they are interprested recursively or not.
A typical case is that of auxiliary verbs, which never depend on each other.

<div id="s3a" class="sd-parse">
She could have been injured .
aux(injured, could)
aux(injured, have)
auxpass(injured, been)
</div>

Note that copula verbs, despite being dependents of their predicates, are treated as main verbs in 
this respect and take auxiliaries as dependents. The general rule is that an auxiliary should always
attach to a verb (if there is one).

<div id="s3b" class="sd-parse">
She could have been sick .
aux(been, could)
aux(been, have)
cop(sick, been)
</div>

However, there are four important exceptions to the rule that function words do not 
take dependents:

  1. Multiword function words
  2. Coordinated function words
  3. Function word modifiers
  4. Promotion by head elision

### Multiword Function Words

The word forms that make up a fixed multiword expression are connected into a head-initial structure
using the special dependency relation `mwe` (see below). When the multiword expression is a functional element,
the initial word form will then superficially look like a function word with dependents.

<div id="s6" class="sd-parse">
We had a nice time in spite of the rain .
case(rain,in)
mwe(in,spite)
mwe(in,of)
nmod(had,rain)
</div>

### Coordinated Function Words

Head coordination is a syntactic process that can apply to almost any word category, including
function words like conjunctions and prepositions. 

<div id="s4a" class="sd-parse">
She drove to and from work .
case(work,to)
conj(to, from)
cc(to, and)
</div>

<div id="s4b" class="sd-parse">
I will do that if and when it happens .
mark(happens,if)
conj(if, when)
cc(if, and)
</div>

### Function Word Modifiers

Certain types of function words can take a restricted class of modifiers, mainly of the types `advmod` and `neg`.
A typical case is that of modified determiners like _exactly two (papers)_ and _not every (linguist)_.

<div id="s7a" class="sd-parse">
exactly two papers
det(papers, two)
advmod(two, exactly)
</div>

<div id="s7b" class="sd-parse">
not every linguist
det(linguist, every)
neg(every, not)
</div>

Function word modifiers should be used restrictively, and an analysis where the modifier attaches to the head word
(and is understood as modifying the entire phrase) should always be preferred if possible. For example, in a case
like _slightly after midnight_, the modifier _slightly_ can be understood as modifying the temporal phrase 
_after midnight_, in analogy with _slightly late_. Hence, the adverb should be attached to _midnight_, which is
the head of _after midnight_.

<div id="s7c" class="sd-parse">
slightly after midnight
case(midnight, after)
advmod(midnight, slightly)
</div>

<div id="s7d" class="sd-parse">
slightly late
advmod(late, slightly)
</div>

We expect modifiers to be possible for words with the grammatical functions `case`, `det`, and `num`.
By contrast, we do not expect to see modifiers for `aux`, `auxpass`, `cc`, and `mark`.

### Promotion by Head Elision

When the natural head of a function word is elided, the function word will be "promoted"
to the function normally assumed by the content word head. This type of analysis should 
in general be preferred over an analysis using the `remnant` relation, because it disrupts
the structure less. The remnant analysis should be used only when there is no function word 
that can be promoted. The following examples illustrate promotion of auxiliaries, prepositions
and subordinating conjunctions.

<div id="s5a" class="sd-parse">
Bill could not answer , but Ann could .
nsubj(answer, Bill)
aux(answer, could-2)
conj(answer, could-8)
nsubj(could-8, Ann)
</div>

<div id="s5b" class="sd-parse">
The address she wrote to .
relcl(address, wrote)
nsubj(wrote, she)
nmod(wrote, to)
</div>

<div id="s5c" class="sd-parse">
I know how .
nsubj(know, I)
ccomp(know, how)
</div>

## Special Relations

Some of the universal relations do not really encode syntactic dependency relations but are used to represent 
punctuation, various kinds of multiword units, or unanalyzable segments. The use of these relations is subject 
to special restrictions explained below.

Tokens with the dependency relation `punct` can never have dependents.

The following types of expressions are always annotated in a head-initial structure, where all non-first elements
depend on the first, and where only the first element can have dependents:

1. Fixed multiword expressions (`mwe`)
2. Multiword names (`name`)
3. Foreign phrases (`foreign`)

<div id="s8a" class="sd-parse">
We had a nice time in spite of the rain .
case(rain,in)
mwe(in,spite)
mwe(in,of)
nmod(had,rain)
</div>

<div id="s8b" class="sd-parse">
Martin Luther King had a dream .
nsubj(had,Martin)
name(Martin,Luther)
name(Luther,King)
</div>

<div id="s8c" class="sd-parse">
She said qwe rty yui .
dobj(said,qwe)
foreign(qwe,rty)
foreign(qwe,yui)
</div>

In contrast, compounds are annotated to show their modification structure, including a regular concept of head:

<div id="s9" class="sd-parse">
I bought a computer disk drive enclosure .
nsubj(bought, I)
det(enclosure, a)
compound(drive, computer)
compound(drive, disk)
compound(enclosure, drive)
dobj(bought, enclosure)
</div>