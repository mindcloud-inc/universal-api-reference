# Create Contact with Startquestion

Creates a contact in Startquestion.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/add`
- **Base URL:** `https://www.startquestion.com/api/v2`
- **Official documentation:** [Create Contact](https://help.startquestion.com/en/articles/5810000-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Contact email address. |
| `label1` | query | `string` | no | First label value. |
| `label2` | query | `string` | no | Second label value. |
| `label3` | query | `string` | no | Third label value. |
