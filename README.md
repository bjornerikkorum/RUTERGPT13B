---
license: llama2
tags:
- pytorch
- llama
- llama-2
- norwegian
- norsk
datasets:
- NbAiLab/norwegian-alpaca
- RuterNorway/OpenOrcaNo-15k
language:
- en
- 'no'
pipeline_tag: text-generation
---
# Llama 2 13b Chat Norwegian
Llama-2-13b-chat-norwegian is a variant of [Meta](https://huggingface.co/meta-llama)´s [Llama 2 13b Chat](https://huggingface.co/meta-llama/Llama-2-13b-chat-hf) model, finetuned on a mix of norwegian datasets created in [Ruter AI Lab](https://ruter.no) the summer of 2023.

The model is tuned to understand and generate text in Norwegian. It's trained for one epoch on norwegian-alpaca + 15000 samples of machine-translated data from OpenOrca. A small subset of custom-made instructional data is also included.

For other versions of this model see:
* [Llama-2-13b-chat-norwegian](https://huggingface.co/RuterNorway/Llama-2-13b-chat-norwegian)
* [Llama-2-13b-chat-norwegian-LoRa](https://huggingface.co/RuterNorway/Llama-2-13b-chat-norwegian-LoRa)
* [Llama-2-13b-chat-norwegian-GPTQ](https://huggingface.co/RuterNorway/Llama-2-13b-chat-norwegian-GPTQ)


## Data
* Norwegian alpaca
* 15k Norwegian OpenOrcra (to be released)
* Small subset of custom made instructional data

## Intended Use
This model is intended for commercial and research use in Norwegian and can be used as an assistant-like chat.

## Prompt Template
Llama2 Chat uses a new prompt format:

```
<s>[INST] <<SYS>>
You are a helpful, respectful and honest assistant. Always answer as helpfully as possible, while being safe. Your answers should not include any harmful, unethical, racist, sexist, toxic, dangerous, or illegal content. Please ensure that your responses are socially unbiased and positive in nature.
If a question does not make any sense, or is not factually coherent, explain why instead of answering something not correct. If you don't know the answer to a question, please don't share false information. Please answer in the same language as the user.
<</SYS>>
This is a test question[/INST] This is a answer </s><s>
```
See also the original implementation [here](https://github.com/facebookresearch/llama/blob/main/llama/generation.py#L213).

We also implemented the alpaca prompt format, which the model supports.:
```
### Instruction:
Summarize following text.
### Input:
Text to be summarized
### Response:
```

## Why this model?
As a Norwegian company, we understand firsthand the pressing need for powerful language models tailored to specific languages. Our primary focus is on the Norwegian linguistic landscape. In the age of digitization, languages that lack robust, open-source models can risk becoming marginalized. This is why we're introducing this open-source Norwegian model. We believe that by making such resources freely accessible, we can democratize information, foster innovation, and create a more inclusive digital ecosystem. Our aspiration is for this model to serve as a foundational resource for future specialized Norwegian models. Ultimately, our goal is to bolster the Norwegian NLP community and facilitate the smoother integration of Norwegian models into diverse projects.

## Limitations
*   This is an LLM, not a knowledge model. It can not be expected to have more information about Norway than the basemodel.
*   It will generally preform better on tasks that involves summarization, question answering and chat, than on tasks that requires more knowledge about Norway, specific domains, or tasks where the model can answer freely.
*   The data used for training is machine translated, and may contain grammatical errors and other errors.
*   The model is released as is, and would in most cases need prompt tuning to achieve optimal results.


## License
Llama 2 is licensed under the LLAMA 2 [Community License](https://ai.meta.com/resources/models-and-libraries/llama-downloads/), Copyright © Meta Platforms, Inc. All Rights Reserved.
See the original [model card](https://huggingface.co/meta-llama/Llama-2-13b) for more information.

From [norwegian-alpaca](https://huggingface.co/NbAiLab/norwegian-alpaca) we also note that "the current version uses OpenAI's gpt-3.5-turbo; hence, this dataset cannot be used to create models that compete in any way against OpenAI."


## Disclaimer
*   The model is available "as is". Ruter As takes no responsibility for further use.
*   During testing, it seems that the safeguards implemented by Meta, still work as expected in this model. However, we want to point to the Ethical Considerations and Limitations from the origenal model card:
```
Llama 2 is a new technology that carries risks with use. Testing conducted to date has been in English, and has not covered, nor could it cover all scenarios.
For these reasons, as with all LLMs, Llama 2’s potential outputs cannot be predicted in advance, and the model may in some instances produce inaccurate, biased or other objectionable responses to user prompts.
Therefore, before deploying any applications of Llama 2, developers should perform safety testing and tuning tailored to their specific applications of the model.
Please see the Responsible Use Guide available at https://ai.meta.com/llama/responsible-use-guide/
```
## Credits
This model was made at Ruters AI Lab which is a part of Ruters Data & AI division.

___
# Llama 2 13b Chat Norwegian (Norsk)
Llama-2-13b-chat-norwegian er en versjon av [Meta](https://huggingface.co/meta-llama) sin [Llama 2 13b Chat](https://huggingface.co/meta-llama/Llama-2-13b-chat-hf) model, finetuned på en kombinasjon av diverse norske datasett. Modellen ble laget i [Ruter AI Lab](https://ruter.no) 2023.

Modellen er finetuned til å forstå og generere tekst på Norsk. Den er trent i én epoch med norwegian-alpaca + et utvalg av 15000 maskinoversatt data fra OpenOrca. Det består og av et lite sett med selvlagde instruksjonsdata

Andre versjoner av modellen:

* [Llama-2-13b-chat-norwegian](https://huggingface.co/RuterNorway/Llama-2-13b-chat-norwegian)
* [Llama-2-13b-chat-norwegian-LoRa](https://huggingface.co/RuterNorway/Llama-2-13b-chat-norwegian-LoRa)
* [Llama-2-13b-chat-norwegian-GPTQ](https://huggingface.co/RuterNorway/Llama-2-13b-chat-norwegian-GPTQ)


## Data
* Norwegian alpaca
* 15k Norwegian OpenOrcra (venter på utgivelse)
* Lite sett med selvlagde instruksjonsdata


## Prompt Mal
Llama2 Chat bruker et nytt prompt format:
```
<s>[INST] <<SYS>>
You are a helpful, respectful and honest assistant. Always answer as helpfully as possible, while being safe. Your answers should not include any harmful, unethical, racist, sexist, toxic, dangerous, or illegal content. Please ensure that your responses are socially unbiased and positive in nature.
If a question does not make any sense, or is not factually coherent, explain why instead of answering something not correct. If you don't know the answer to a question, please don't share false information. Please answer in the same language as the user.
<</SYS>>
This is a test question[/INST] This is a answer </s><s>
```
Se orgianl implementasjon [her](https://github.com/facebookresearch/llama/blob/main/llama/generation.py#L213).

Vi har også implementert alpaca prompt formatet, som også er støttet av modellen.
```
### Instruction:
Summarize following text.
### Input:
Text to be summarized
### Response:
```

## Hvorfor denne modellen?
Som et norsk selskap forstår vi selv det presserende behovet for kraftige språkmodeller tilpasset spesifikke språk. Vårt primære fokus er på det norske språkområdet. I den digitale alderen risikerer språk som mangler robuste, åpne kildekodemodeller å bli marginalisert. Dette er grunnen til at vi nå introduserer denne åpne kildekodemodellen for norsk. Vi tror at ved å gjøre disse ressursene tilgjengelige gratis, kan vi demokratisere informasjonen, fremme innovasjon og skape et mer inkluderende digitalt økosystem. Vår ambisjon er at denne modellen skal tjene som en grunnleggende ressurs for fremtidige spesialiserte norske modeller. Vårt mål er å styrke det norske NLP-miljøet og gjøre det enklere å innlemme norske modeller i ulike prosjekter.

## Begrensninger
*   Dette er en LLM, ikke en kunnskapsmodell. Den kan ikke forventes å ha mer informasjon om Norge enn basismodellen.
*   Den vil generelt prestere bedre på oppgaver som innebærer oppsummering, spørsmålsbesvarelse og chat, enn på oppgaver som krever mer kunnskap om Norge, spesifikke domener, eller oppgaver hvor modellen kan svare fritt.
*   Dataene som brukes til trening er maskinoversatt, og kan inneholde grammatiske feil. Vi har kun gjort en rask manuell sjekk av dataene.
*   Modellen er utgitt som den er, og vil i de fleste tilfeller trenge "prompt tuning" for å oppnå ønskede resultater.

## Lisens
Llama 2 er lisensiert under LLAMA 2 [Community License](https://ai.meta.com/resources/models-and-libraries/llama-downloads/), Copyright © Meta Platforms, Inc. All Rights Reserved.
Se det orginale [modell kortet](https://huggingface.co/meta-llama/Llama-2-13b) for mer informasjon.


Fra [norwegian-alpaca](https://huggingface.co/NbAiLab/norwegian-alpaca) vil vi gjøre oppmerksomme på at "the current version uses OpenAI's gpt-3.5-turbo; hence, this dataset cannot be used to create models that compete in any way against OpenAI."


## Ansvarsfraskrivelse
*   Modellen tilgjengeliggjøres «som den er». Ruter As tar ikke noe ansvar for videre bruk.
*   Under testingen virket det som sikkerhetstiltakene implementert av Meta fortsatt fungerer som forventet for denne modellen. Vi gjør derimot oppmerksom på de etiske betraktiningene og begrensningene fra det orignale modellkortet:
```
Llama 2 is a new technology that carries risks with use. Testing conducted to date has been in English, and has not covered, nor could it cover all scenarios.
For these reasons, as with all LLMs, Llama 2’s potential outputs cannot be predicted in advance, and the model may in some instances produce inaccurate, biased or other objectionable responses to user prompts.
Therefore, before deploying any applications of Llama 2, developers should perform safety testing and tuning tailored to their specific applications of the model.
Please see the Responsible Use Guide available at https://ai.meta.com/llama/responsible-use-guide/
```