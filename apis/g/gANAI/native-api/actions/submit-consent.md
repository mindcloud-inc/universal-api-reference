# Submit Consent with GAN.AI

Submits a consent video to GAN.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/consents/submit_consent`
- **Base URL:** `https://os.gan.ai`
- **Official documentation:** [Submit Consent](https://developer.gan.ai/api-reference/consent/submit-consent)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `avatar_id` | query | `string` | yes |
| `consent_video` | query | `string` | yes |
