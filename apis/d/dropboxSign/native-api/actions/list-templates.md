# List Templates with Dropbox Sign

Retrieves templates from Dropbox Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/template/list`
- **Base URL:** `https://api.hellosign.com/v3`
- **Official documentation:** [List Templates](https://developers.hellosign.com/api/reference/operation/templateList/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | query | `string` | no | Which account to return Templates for. Use all for all team members. |
| `query` | query | `string` | no | Search terms used to filter templates. |
