# Get Emails with Datalyse

Retrieves emails from Datalyse by folder.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/emails/get.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Get Emails](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_value` | body | `string` | no | Search in subject (optional) |
| `type` | body | `string` | no | Folder: "inbox" (default) or "sent" |
| `unread_only` | body | `string` | no | Show only unread, set to "y" (optional) |
| `var_page` | body | `string` | no | Page number |
| `var_resultspage` | body | `string` | no | Maximum number of results |
