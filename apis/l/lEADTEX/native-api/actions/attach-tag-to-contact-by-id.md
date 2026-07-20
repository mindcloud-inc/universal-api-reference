# Attach Tag To Contact By ID with LEADTEX

Attaches a tag to a contact in LEADTEX by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/attachTagToContact?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Attach Tag To Contact By ID](https://docs.leadteh.ru/rabota-s-api/kontakty/tegi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `number` | yes | ID of the contact to tag. |
| `tag_id` | body | `number` | yes | ID of the tag to attach. |
