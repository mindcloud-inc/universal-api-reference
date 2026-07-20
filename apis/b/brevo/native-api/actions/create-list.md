# Create List with Brevo

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/contacts/lists`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Create List](https://developers.brevo.com/reference/create-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | body | `number` | yes | Brevo folder ID that will contain the list. |
| `name` | body | `string` | yes | List name. |
