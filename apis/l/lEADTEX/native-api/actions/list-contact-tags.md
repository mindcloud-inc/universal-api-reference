# List Contact Tags with LEADTEX

Retrieves tags for a specific contact in LEADTEX.

## Endpoint

- **Method:** `GET`
- **Path:** `/getContactTags?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [List Contact Tags](https://docs.leadteh.ru/rabota-s-api/kontakty/tegi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | query | `number` | yes | ID of the contact whose tags should be returned. |
