# Create contact list with Webex Interact

Creates a new contact list in Webex Interact.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/v1/lists/create`
- **Base URL:** `https://api.webexinteract.com`
- **Official documentation:** [Create contact list](https://docs.webexinteract.com/reference/lists-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name for the new contact list. Maximum 120 characters. |
