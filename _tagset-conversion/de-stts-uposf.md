---
layout: base
title: 'Tagset de::stts conversion to universal POS tags and features'
---

<a href="index.html">all tables</a>

## Tagset de::stts

**Disclaimer:**
This conversion table was generated automatically via Interset.
It uses only tags (+ features) as input, therefore it is only an approximation.
Some tags can only be mapped if we also know the lemma or the syntactic context; such information has not been available here.
The table requires manual postprocessing in order to provide accurate and complete information.

Tagset <tt>de::stts</tt>, total 54 tags.

<table>
  <tr><td>$(</td><td>=&gt;</td><td>PUNCT</td><td>PunctType=Brck</td><td>_``, '', *RRB*, *LRB*, -_</td></tr>
  <tr><td>$,</td><td>=&gt;</td><td>PUNCT</td><td>PunctType=Comm</td><td>_,_</td></tr>
  <tr><td>$.</td><td>=&gt;</td><td>PUNCT</td><td>PunctType=Peri</td><td>_., :, ?, ;, !_</td></tr>
  <tr><td>ADJA</td><td>=&gt;</td><td>ADJ</td><td>_</td><td>_neuen, neue, deutschen, ersten, anderen_</td></tr>
  <tr><td>ADJD</td><td>=&gt;</td><td>ADJ</td><td>Variant=Short</td><td>_gut, rund, knapp, deutlich, möglich_</td></tr>
  <tr><td>ADV</td><td>=&gt;</td><td>ADV</td><td>_</td><td>_auch, nur, noch, so, aber_</td></tr>
  <tr><td>APPO</td><td>=&gt;</td><td>ADP</td><td>AdpType=Post</td><td>_zufolge, nach, gegenüber, wegen, über_</td></tr>
  <tr><td>APPR</td><td>=&gt;</td><td>ADP</td><td>AdpType=Prep</td><td>_in, von, mit, für, auf_</td></tr>
  <tr><td>APPRART</td><td>=&gt;</td><td>ADP</td><td>AdpType=Prep|PronType=Art</td><td>_im, am, zum, zur, vom_</td></tr>
  <tr><td>APZR</td><td>=&gt;</td><td>ADP</td><td>AdpType=Circ</td><td>_an, hinaus, aus, her, heraus_</td></tr>
  <tr><td>ART</td><td>=&gt;</td><td>DET</td><td>PronType=Art</td><td>_der, die, den, des, das_</td></tr>
  <tr><td>CARD</td><td>=&gt;</td><td>NUM</td><td>NumType=Card</td><td>_000, zwei, drei, vier, fünf_</td></tr>
  <tr><td>FM</td><td>=&gt;</td><td>X</td><td>Foreign=Yes</td><td>_New, of, de, Times, the_</td></tr>
  <tr><td>ITJ</td><td>=&gt;</td><td>INTJ</td><td>_</td><td>_naja, Ach, äh, Na, piep_</td></tr>
  <tr><td>KOKOM</td><td>=&gt;</td><td>CONJ</td><td>ConjType=Comp</td><td>_als, wie, denn, wir_</td></tr>
  <tr><td>KON</td><td>=&gt;</td><td>CONJ</td><td>_</td><td>_und, oder, sondern, sowie, aber_</td></tr>
  <tr><td>KOUI</td><td>=&gt;</td><td>SCONJ</td><td>_</td><td>_um, ohne, statt, anstatt, Ums_</td></tr>
  <tr><td>KOUS</td><td>=&gt;</td><td>SCONJ</td><td>_</td><td>_daß, wenn, weil, ob, als_</td></tr>
  <tr><td>NE</td><td>=&gt;</td><td>PROPN</td><td>_</td><td>_SPD, Deutschland, USA, dpa, Bonn_</td></tr>
  <tr><td>NN</td><td>=&gt;</td><td>NOUN</td><td>_</td><td>_Prozent, Mark, Millionen, November, Jahren_</td></tr>
  <tr><td>PAV</td><td>=&gt;</td><td>ADV</td><td>PronType=Dem</td><td>__</td></tr>
  <tr><td>PDAT</td><td>=&gt;</td><td>DET</td><td>PronType=Dem</td><td>_dieser, diese, diesem, dieses, diesen_</td></tr>
  <tr><td>PDS</td><td>=&gt;</td><td>PRON</td><td>PronType=Dem</td><td>_das, dies, die, diese, der_</td></tr>
  <tr><td>PIAT</td><td>=&gt;</td><td>DET</td><td>PronType=Ind,Neg,Tot</td><td>_keine, mehr, alle, kein, beiden_</td></tr>
  <tr><td>PIDAT</td><td>=&gt;</td><td>DET</td><td>AdjType=Pdt|PronType=Ind,Neg,Tot</td><td>__</td></tr>
  <tr><td>PIS</td><td>=&gt;</td><td>PRON</td><td>PronType=Ind,Neg,Tot</td><td>_man, allem, nichts, alles, mehr_</td></tr>
  <tr><td>PPER</td><td>=&gt;</td><td>PRON</td><td>PronType=Prs</td><td>_es, sie, er, wir, ich_</td></tr>
  <tr><td>PPOSAT</td><td>=&gt;</td><td>DET</td><td>Poss=Yes|PronType=Prs</td><td>_ihre, seine, seiner, ihrer, ihren_</td></tr>
  <tr><td>PPOSS</td><td>=&gt;</td><td>PRON</td><td>Poss=Yes|PronType=Prs</td><td>_ihren, Seinen, seinem, unsrigen, meiner_</td></tr>
  <tr><td>PRELAT</td><td>=&gt;</td><td>DET</td><td>PronType=Rel</td><td>_deren, dessen, die_</td></tr>
  <tr><td>PRELS</td><td>=&gt;</td><td>PRON</td><td>PronType=Rel</td><td>_die, der, das, dem, denen_</td></tr>
  <tr><td>PRF</td><td>=&gt;</td><td>PRON</td><td>PronType=Prs|Reflex=Yes</td><td>_sich, uns, mich, mir, dich_</td></tr>
  <tr><td>PTKA</td><td>=&gt;</td><td>PART</td><td>_</td><td>_zu, am, allzu, Um_</td></tr>
  <tr><td>PTKANT</td><td>=&gt;</td><td>PART</td><td>PartType=Res</td><td>_nein, ja, bitte, Gewiß, Also_</td></tr>
  <tr><td>PTKNEG</td><td>=&gt;</td><td>PART</td><td>Negative=Neg</td><td>_nicht_</td></tr>
  <tr><td>PTKVZ</td><td>=&gt;</td><td>PART</td><td>PartType=Vbp</td><td>_an, aus, ab, vor, auf_</td></tr>
  <tr><td>PTKZU</td><td>=&gt;</td><td>PART</td><td>PartType=Inf</td><td>_zu, zur, zum_</td></tr>
  <tr><td>PWAT</td><td>=&gt;</td><td>DET</td><td>PronType=Int</td><td>_welche, welchen, welcher, wie, welchem_</td></tr>
  <tr><td>PWAV</td><td>=&gt;</td><td>ADV</td><td>PronType=Int</td><td>_wie, wo, warum, wobei, wonach_</td></tr>
  <tr><td>PWS</td><td>=&gt;</td><td>PRON</td><td>PronType=Int</td><td>_was, wer, wem, wen, welches_</td></tr>
  <tr><td>TRUNC</td><td>=&gt;</td><td>X</td><td>Hyph=Yes</td><td>_Staats-, Industrie-, Finanz-, Öl-, Lohn-_</td></tr>
  <tr><td>VAFIN</td><td>=&gt;</td><td>AUX</td><td>Mood=Ind|VerbForm=Fin</td><td>_ist, hat, wird, sind, sei_</td></tr>
  <tr><td>VAIMP</td><td>=&gt;</td><td>AUX</td><td>Mood=Imp|VerbForm=Fin</td><td>_Seid, werde, Sei_</td></tr>
  <tr><td>VAINF</td><td>=&gt;</td><td>AUX</td><td>VerbForm=Inf</td><td>_werden, sein, haben, worden, Dabeisein_</td></tr>
  <tr><td>VAPP</td><td>=&gt;</td><td>AUX</td><td>Aspect=Perf|VerbForm=Part</td><td>_worden, gewesen, geworden, gehabt, werden_</td></tr>
  <tr><td>VMFIN</td><td>=&gt;</td><td>VERB</td><td>Mood=Ind|VerbForm=Fin|VerbType=Mod</td><td>_kann, soll, will, muß, sollen_</td></tr>
  <tr><td>VMINF</td><td>=&gt;</td><td>VERB</td><td>VerbForm=Inf|VerbType=Mod</td><td>_können, müssen, wollen, dürfen, sollen_</td></tr>
  <tr><td>VMPP</td><td>=&gt;</td><td>VERB</td><td>Aspect=Perf|VerbForm=Part|VerbType=Mod</td><td>_gewollt_</td></tr>
  <tr><td>VVFIN</td><td>=&gt;</td><td>VERB</td><td>Mood=Ind|VerbForm=Fin</td><td>_sagte, gibt, geht, steht, kommt_</td></tr>
  <tr><td>VVIMP</td><td>=&gt;</td><td>VERB</td><td>Mood=Imp|VerbForm=Fin</td><td>_siehe, sprich, schauen, Sagen, gestehe_</td></tr>
  <tr><td>VVINF</td><td>=&gt;</td><td>VERB</td><td>VerbForm=Inf</td><td>_machen, lassen, bleiben, geben, bringen_</td></tr>
  <tr><td>VVIZU</td><td>=&gt;</td><td>VERB</td><td>VerbForm=Inf</td><td>_einzusetzen, durchzusetzen, aufzunehmen, abzubauen, umzusetzen_</td></tr>
  <tr><td>VVPP</td><td>=&gt;</td><td>VERB</td><td>Aspect=Perf|VerbForm=Part</td><td>_gemacht, getötet, gefordert, gegeben, gestellt_</td></tr>
  <tr><td>XY</td><td>=&gt;</td><td>X</td><td>_</td><td>_dpa, ap, afp, rtr, wb_</td></tr>
</table>