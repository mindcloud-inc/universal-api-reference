# Detach Tag From Contact with LEADTEX

Deletes a tag from a contact in LEADTEX by name.

## Endpoint

- **Method:** `POST`
- **Path:** `/detachTagFromContact?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Detach Tag From Contact](https://docs.leadteh.ru/rabota-s-api/kontakty/tegi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `number` | yes | ID of the contact to untag. |
| `name` | body | `string` | yes | Name of the tag to detach. |
