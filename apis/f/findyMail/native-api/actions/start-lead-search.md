# Start Lead Search with FindyMail

Starts a lead search in FindyMail.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/intellimatch/search`
- **Base URL:** `https://app.findymail.com`
- **Official documentation:** [Start Lead Search](https://www.findymail.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Natural-language lead search query. |
| `limit` | body | `number` | no | Maximum number of lead results to request. |
| `config.find_contact` | body | `boolean` | no | Whether FindyMail should find a contact for each matching company. |
| `config.find_email` | body | `boolean` | no | Whether FindyMail should find an email for each matching contact. |
