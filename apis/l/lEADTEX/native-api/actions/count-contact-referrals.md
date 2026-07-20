# Count Contact Referrals with LEADTEX

Retrieves the total referrals in a contact's network in LEADTEX.

## Endpoint

- **Method:** `POST`
- **Path:** `/getCountReferrals?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Count Contact Referrals](https://docs.leadteh.ru/rabota-s-api/kontakty/referalnaya-sistema/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `number` | yes | ID of the contact whose referral network should be counted. |
