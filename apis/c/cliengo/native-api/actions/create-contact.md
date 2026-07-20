# Create Contact with Cliengo

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.cliengo.com/1.0`
- **Official documentation:** [Create Contact](https://developers.cliengo.com/reference/contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `websiteId` | body | `string` | yes | The contact's source website id. |
| `name` | body | `string` | no | Contact's name. |
| `email` | body | `string` | no | Contact's email. |
| `message` | body | `string` | no | Initial message for the contact. |
