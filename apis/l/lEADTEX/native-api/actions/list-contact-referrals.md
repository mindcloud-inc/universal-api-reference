# List Contact Referrals with LEADTEX

Retrieves referrals for a specific contact in LEADTEX.

## Endpoint

- **Method:** `POST`
- **Path:** `/getReferrals?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [List Contact Referrals](https://docs.leadteh.ru/rabota-s-api/kontakty/referalnaya-sistema/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `number` | yes | ID of the contact whose referrals should be returned. |
