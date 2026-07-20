# Get Contact Referrers with LEADTEX

Retrieves referrers for a specific contact in LEADTEX.

## Endpoint

- **Method:** `GET`
- **Path:** `/getReferrers?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Get Contact Referrers](https://docs.leadteh.ru/rabota-s-api/kontakty/referalnaya-sistema/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | query | `number` | yes | ID of the contact whose referrers should be returned. |
| `depth` | query | `number` | yes | Referral tree depth from 1 to 10. |
