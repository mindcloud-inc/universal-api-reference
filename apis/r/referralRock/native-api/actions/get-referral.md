# Get Referral with Referral Rock

Retrieves a referral from Referral Rock by email, referral ID, or external ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/referral/single`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [Get Referral](https://api.referralrock.com/Help/Api/GET-api-referral-single_email_referralId_externalId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | The email address of the referral. |
| `externalId` | query | `string` | no | The external identifier of the referral. |
| `referralId` | query | `string` | no | The unique identifier of the referral. |
