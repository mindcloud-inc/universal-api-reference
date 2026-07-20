# Create Offline Contact with Startquestion

Creates a contact in Startquestion for offline distribution.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/add-offline`
- **Base URL:** `https://www.startquestion.com/api/v2`
- **Official documentation:** [Create Offline Contact](https://help.startquestion.com/en/articles/5810000-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_token` | query | `string` | yes | Offline distribution user token. |
| `label1` | query | `string` | no | First label value. |
| `label2` | query | `string` | no | Second label value. |
