---
title: Bing Speech API in Microsoft Cognitive Services | Microsoft Docs
description: Use the Bing Speech API to add speech-driven actions to your apps, including real-time interaction with users.
services: cognitive-services
author: priyaravi20
manager: yanbo

ms.service: cognitive-services
ms.technology: speech
ms.topic: article
ms.date: 09/14/2017
ms.author: prrajan
---
# Bing Speech API overview

Microsoft Speech API provides you easy-to-use APIs to create powerful speech-enabled features in your applications, like voice command control, user dialog using natual speech conversation, and speech transcription and dictation. The Microsoft Speech API supports both *Speech to Text* and *Text to Speech* conversion.

* **Speech to Text** APIs convert human speech to text that can be used as input or commands to control your application.
* **Text to Speech** APIs convert text to audio streams that can be played back to the user of your application.

## Speech to text (speech recognition)
The *Speech to Text* APIs *transcribe* audio streams into text that your application can display to the user or act upon as command input. The *Speech To Text* APIs come in two flavors.

Highlight features: 
* Supports many spoken languages in multiple dialects. For the full list of supported languages in
each recognition mode, see [Recognition Languages](api-reference-rest/bingvoicerecognition.md#recognition-language).
* Applies powerful speech recognition technolgoies that are used by Cortana, Office Dictation, Office Translator, and other Microsoft products.
* Supports multiple recognition modes to enable optimized results in different user scenarios. The *Speech to Text* APIs currently support *interactive*, *conversation*, and *dictation* mode.
* Real-time continuous recognition. The *Speech to Text* supports both recognition of 
* Support adding capitalization and punctuation, masking profanity, and text normalization.

Developers can use both REST API or Microsoft Speech Client Libraries to access APIs for speech to text. 

It supports different use for interactive, conversaton and dictation

Covert short spoken commands (audio length < 15s) without intermit results: REST and Client Libraries
Audio length > 15s: Client Libraries.
Interim results desired. Client Libraries


## Text to speech (speech synthesis)
*Text to Speech* APIs use REST to convert structured text to an audio stream. The APIs provide fast text to speech
conversion in various voices and languages. For the full list of supported languages and voices, see
[Supported Locales and Voice Fonts](api-reference-rest/bingvoiceoutput.md#SupLocales).

### Text to speech API
The maximum amount of audio returned for any single request is 15 seconds.

## Next 
Please follow Get Started to build your first speech enabled application.