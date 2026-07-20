# Add contact to opt-in page's groups with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/opt-in-pages/{pageId}`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Add contact to opt-in page's groups](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | ID of the opt-in page to add contact to its groups |
| `email` | body | `string` | yes | Email of the contact |
| `name` | body | `string` | no | Full name of the contact |
