# Detach Tag From Contact By ID with LEADTEX

Deletes a tag from a contact in LEADTEX by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/detachTagFromContact?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Detach Tag From Contact By ID](https://docs.leadteh.ru/rabota-s-api/kontakty/tegi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `number` | yes | ID of the contact to untag. |
| `tag_id` | body | `number` | yes | ID of the tag to detach. |
