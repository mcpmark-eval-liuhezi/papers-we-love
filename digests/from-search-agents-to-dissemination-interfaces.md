# From Search Agents to Dissemination Interfaces: Understanding Human Trust in Health Information from Conversational Search

**Digest for the reading group — quarterly collection**

## Citation

**Title:** From Search Agents to Dissemination Interfaces: Understanding Human Trust in Health Information from Conversational Search

**Authors:** Xin Sun, Rongjun Ma, Xiaochang Zhao, Janne Lindqvist, Jan de Wit, Zhuying Li, Abdallah El Ali, Jos A. Bosch

**arXiv ID:** [2608.21177](https://arxiv.org/abs/2608.21177) (v1, cs.HC)

**Note:** The manuscript has been accepted for publication in the journal *Behaviour & Information Technology* (BIT).

## TL;DR

Through two mixed-methods lab studies (lab sessions plus semi-structured interviews), this paper examines how people form trust in health information from conversational search — first comparing a traditional search engine (Google) with an LLM-powered conversational agent (ChatGPT/GPT-4o), and then comparing three dissemination interfaces (text-based, speech-based, and embodied) that all draw on the same LLM. The headline result is a double dissociation: people trusted health information from ChatGPT *significantly more* than from Google, yet they trusted the *same* LLM-sourced information most when it was delivered through a plain **text-based** interface, with voice and embodiment actually *reducing* trust relative to text. In other words, users reward the conversational, synthesized, "human-like" *style* of LLM answers while still wanting the control, scannability, and cross-referencing affordances of a text UI — and trust in the information tracks trust in the interface carrying it. Trust also turns out to be **source-dissociated** in conversational search: for Google, trust in the agent correlated with trust in the information, but for ChatGPT the two decoupled. The paper closes with concrete design guidance: be a bridge rather than an oracle, prefer functional over visual anthropomorphism, calibrate to user knowledge and affect, and make personalization privacy-preserving.

## Study 1: Search agents — Google vs. ChatGPT

### Methods

- **Design:** Within-subjects lab study followed by semi-structured interviews, mixing quantitative questionnaires with qualitative thematic analysis.
- **Participants:** N=21, recruited via the institute's recruitment system, English-proficient and experienced with online search (16 female / 5 male; mostly 18–24; majority undergraduate or postgraduate; 42.8% frequent online health seekers).
- **Agents compared:** Google (search engine; "information" here includes results-page snippets plus the content of external websites) and ChatGPT (LLM agent; "information" is exclusively the LLM's directly synthesized textual responses). ChatGPT was used with the GPT-4 model **without** web browsing, on identical desktop/Chrome setups.
- **Tasks:** Six health-related search tasks per participant, drawn from an open-sourced dataset of personal health questions (Yadav et al.) spanning three types: **general health questions**, **symptom/cause-related questions**, and **treatment-related questions**.
- **Measures:** Propensity of trust in technology; perceived trust in health-related information (validated "Trust of Online Health Information" questionnaire, 11 items, α=.95); perceived trust in the search agent ("Model of Online Trust of Health Information Websites," 15 items, α=.62).
- **Analysis:** Shapiro–Wilk and Bartlett assumption checks, two-way repeated-measures ANOVA, paired-samples t-tests, Pearson correlations, and thematic analysis of interview transcripts.

### Findings on trust

- **Significantly higher trust in ChatGPT-sourced health information.** Two-way repeated-measures ANOVA showed a significant main effect of the search agent on trust in the retrieved health information, F(1,20)=6.73, p=.017, η²=.057 — ChatGPT was generally trusted more than Google for health advice.
- **Trust in the agents themselves also differed.** A paired-samples t-test found a significant difference in trust between the two agents as search agents (mean difference 0.27, t(21)=-2.53, p=.02, Cohen's d=0.55).
- **Task type didn't matter.** No significant effect of search-task type on trust (F(2,40)=0.63, p=.480), and no significant agent × task interaction (F(2,40)=0.20, p=.777) — the ChatGPT-over-Google trust advantage was stable across general, symptom, and treatment questions.
- **Source dissociation.** For **Google**, trust in the information correlated significantly with trust in the agent (r(21)=0.63, p=.003). For **ChatGPT**, that correlation was **not** significant (r(21)=0.09, p=.21). The authors call this *source dissociation*: in web search the agent and the external medical websites are structurally separable, so users can judge source credibility independently; conversational search collapses that distinction, and users fall back on trust heuristics (logical flow, professional language, presentation) rather than the agent's reputation.
- **Qualitative themes shaping trust:** prior experience with an agent (positive/negative past encounters, "news and rumors" about ChatGPT, filter bubbles and commercial clutter in Google); information presentation (professional-but-understandable language, passive voice conveying objectivity, hedged answers like "maybe" lowering trust but *over*-confident answers also eroding it, logical structure, visual cues); **search autonomy** (Google gives users the feeling of being their own judge; participants with low prior knowledge preferred ChatGPT's high-synthesis, low-autonomy approach, treating it as a "knowledge scaffold" and a starting point before Googling); **human-like interaction** (dialogue that feels like talking to a friend, contextual follow-ups that make users feel heard); and **personalization** (regional medical-system differences, personal symptoms/allergies, proactive questioning like a human doctor).

## Study 2: Dissemination interfaces — text vs. speech vs. embodied

### Methods

- **Design:** Lab study plus semi-structured interviews, holding the information source constant to isolate the effect of the **dissemination interface**.
- **Participants:** N=20 (16 female / 4 male; all aged 18–34, 80% in the 18–24 bracket; 55% undergraduate, 45% postgraduate; drawn from business/law, arts, health/medical science, STEM and other fields; 75% occasional online health seekers).
- **Interfaces compared:** (a) **text-based** — a web-based chat interface for text-only interaction; (b) **speech-based** — an Amazon Echo Dot with wake words disabled and only the standard light ring for feedback, minimizing brand association; (c) **embodied** — a custom-built physical body with an internal speaker and a smartphone "face" showing simple expressions, deliberately avoiding hyper-realistic anthropomorphism. **All three were powered by the same GPT-4o model** to ensure generation consistency, so any trust differences are attributable to the interface.
- **Tasks:** Aligned with Study 1 — health questions across the same three types (general, symptom, treatment).
- **Measures:** Aligned with Study 1, plus familiarity with each interface, usability level, trust in the interface, and intention to use it for health information search; recognition-accuracy and follow-up-query counts for the speech and embodied conditions.
- **Analysis:** Mixed Linear Model (MixedLM) regression controlling for usability, trust in the interface, and familiarity; Pearson correlations; mediation analysis; thematic analysis of interviews.

### Findings on trust

- **Trust decreased as modality richness increased.** Mean trust in the health information was highest for the **text-based** interface (M=4.19, SD=.42), followed by **speech-based** (M=4.13, SD=.46) and **embodied** (M=4.00, SD=.48). Trust in the interfaces themselves followed the same ordering: text M=3.73 (SD=.37), speech M=3.57 (SD=.46), embodied M=3.56 (SD=.44).
- **Significant pairwise differences (MixedLM).** Trust in health information differed significantly between the text-based and embodied interfaces (β=.189, p=.035) and between the speech-based and embodied interfaces (β=.180, p=.002).
- **Usability is the mechanism.** Usability significantly predicted trust in the information (β=.187, p=.004), and a mediation analysis showed usability **fully mediates** the relationship between interface type and trust in information (significant indirect effect β=.154, p<.001; non-significant direct effect β=.098, p=.277). Usability was highest for text (M=4.05, SD=.43) versus speech (M=3.55, SD=.67) and embodied (M=3.55, SD=.63).
- **Trust in the information tracks trust in the interface — across all modalities.** Trust in information correlated with trust in the interface for text (r(20)=.58, p<.01), speech (r(20)=.52, p<.05), and embodied (r(20)=.76, p<.01); trust in the information also correlated with usability for text (r(20)=.47, p<.05) and embodied (r(20)=.64, p<.01).
- **Task type, again, didn't matter.** No significant difference in trust across the three types of health questions (p=.510) — the text-first trust pattern is a generalized behavior, not a task-specific anomaly.
- **Familiarity and behavioral signals.** Participants were most familiar with text (M=3.60), then speech (M=2.35), then embodied (M=1.60), and most intended to *use* text (M=3.55), then speech (M=3.05), then embodied (M=2.70). Speech recognition accuracy was 83.3% vs. 88.3% for the embodied interface, but follow-up questions were most common with the **embodied** interface (14 tasks) vs. text (10) and speech (7) — embodiment invites engagement even as it erodes trust.
- **Qualitative themes:** familiarity with the interface (text resembling WhatsApp chats and professional literature); usability (text's simplicity; usability as the make-or-break factor for less familiar speech/embodied UIs); presentation style (numbered lists that work in text cause information overload when spoken — storytelling and up-front summaries worked better vocally); modality of processing (reading takes less effort than listening; text lets users scroll back, cross-compare, and share with a clinician, whereas speech and embodiment demand active listening with no rewind); and human-like features (embodiment strengthened the sense of human interaction and generated more follow-ups, but raised concerns about voice, appearance, the uncanny valley, and "constant listening" surveillance/privacy risks). Participants preferred embodied interfaces that balanced human-like and robotic features — neutral, professional, well-matched voices and movements.

## Practical takeaways for conversational search interface design

- **Don't assume modality richness buys trust.** The MAIN-model intuition that more modality and social cues increase credibility did not hold here — text beat speech and embodiment. In high-stakes domains like health, the scannability, revisability, and cross-referencing affordances of text outweigh the "naturalness" of voice or avatars. Default to text-first and treat richer modalities as opt-in enhancements rather than replacements.
- **Design usability for trust, not just efficiency.** Usability fully mediated the interface-type → trust-in-information effect. If your CUI is hard to use, users will discount the information it carries, however accurate it is.
- **Bridge search and verification instead of replacing it.** Users treat LLMs as a starting point, not a final authority. Add clickable provenance so medical claims trace back to sources inside the chat flow, and proactively offer verification cues for high-stakes queries (e.g., "This is a complex condition; would you like to see clinical guidelines?"). This converts the source-dissociation problem into a feature.
- **Aim for functional, not visual, anthropomorphism.** Users want the *conversational patterns* of a good clinician — empathy, reassurance, breaking down complex diagnoses — but distrust avatars and ambiguous identities. Keep an explicit "I am an AI" identity label, avoid the uncanny valley, and let the warmth live in the tone rather than the face.
- **Calibrate to the user's expertise and affect.** Implement dynamic scaffolding: implicitly detect expertise (e.g., use of medical terminology) and adapt response complexity, and add affect-aware calibration that prioritizes "affective safety" when distress or high-stakes symptoms are detected, to mitigate cyberchondria rather than amplify it.
- **Watch the confidence dial.** Hedging ("maybe," "I'm not sure") lowers trust, but over-confident causal claims do too — especially in medicine, where "the answer is never so straightforward." Calibrated confidence is a trust feature, not a hedge.
- **Personalize, but make it privacy-preserving — and legible.** Participants wanted region- and symptom-aware answers and proactive follow-up questions, yet feared surveillance and data leakage, especially from always-listening voice and camera-bearing embodiment. Offer incognito health modes and explicit forgetting mechanisms for sensitive queries, surface visual cues when prior symptom data informs a response, and move beyond binary accept/reject consent toward granular, context-sensitive controls.
- **Adapt presentation to the modality.** Numbered lists suit text but overload speech; use storytelling and lead-with-the-summary for spoken output, and let users mix modalities (type a question, hear the answer, see it transcribed on a screen).
- **Trust is two-layered — measure both.** Because trust in the agent and trust in the information can dissociate, evaluating a conversational system on response accuracy alone will miss the interface-level trust dynamics that actually drive adoption and reliance.

## BibTeX

```bibtex
@misc{sun2026from,
  title = {From Search Agents to Dissemination Interfaces: Understanding Human Trust in Health Information from Conversational Search},
  author = {Xin Sun and Rongjun Ma and Xiaochang Zhao and Janne Lindqvist and Jan de Wit and Zhuying Li and Abdallah El Ali and Jos A. Bosch},
  year = {2026},
  eprint = {2608.21177},
  archivePrefix = {arXiv},
  primaryClass = {cs.HC},
  url = {https://arxiv.org/abs/2608.21177}
}
```
