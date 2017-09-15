---
title: How to authenticate to use Speech Client APIs | Microsoft Docs
description: How to authenticate to use Speech Client APIs
services: cognitive-services
author: zhouwang
manager: wolfma

ms.service: cognitive-services
ms.technology: speech
ms.topic: article
ms.date: 09/15/2017
ms.author: zhouwang
---
# How to authenticate to use Speech Client APIs

## Using Subscription Key
#### Subscribe to Speech API and get a free trial subscription key
To access the REST end point, you must subscribe to Speech API which is part of Microsoft Cognitive Services (previously Project Oxford). After subscribing, you will have the necessary subscription keys to execute this operation. Both the primary and secondary keys can be used. For subscription and key management details, see [Subscriptions](https://azure.microsoft.com/en-us/try/cognitive-services/). 

## Authorization 

In addition to the standard web socket handshake headers, speech requests require an *Authorization* header. Connection requests without this header are rejected 
by the service with a 403 Forbidden HTTP response.

The *Authorization* header must contain a JSON Web Token (JWT) access token.

For information about subscribing and obtaining API keys that are used to retrieve valid JWT access tokens, see [Get Started for Free](https://www.microsoft.com/cognitive-services/en-US/sign-up?ReturnUrl=/cognitive-services/en-us/subscriptions?productId=%2fproducts%2fBing.Speech.Preview).

The API key is passed to the token service. For example:

```
POST https://api.cognitive.microsoft.com/sts/v1.0/issueToken
Content-Length: 0
```

The required header information for token access is as follows.

Name	| Format	| Description
---------|---------|--------
Ocp-Apim-Subscription-Key |	ASCII	| Your subscription key

The token service returns the JWT access token as `text/plain`. Then the JWT is passed as a `Base64 access_token` to the handshake as an authorization header prefixed with the string `Bearer`. For example:

`Authorization: Bearer [Base64 access_token]`