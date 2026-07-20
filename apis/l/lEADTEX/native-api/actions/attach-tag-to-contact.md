# Attach Tag To Contact with LEADTEX

Attaches a tag to a contact in LEADTEX by name.

## Endpoint

- **Method:** `POST`
- **Path:** `/attachTagToContact?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Attach Tag To Contact](https://docs.leadteh.ru/rabota-s-api/kontakty/tegi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `number` | yes | ID of the contact to tag. |
| `name` | body | `string` | yes | Name of the tag to attach. If it does not exist, LEADTEX creates it. |
