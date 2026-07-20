# List Contacts with Trustmary

Retrieves contacts from Trustmary.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.trustmary.io/v1`
- **Official documentation:** [List Contacts](https://help.trustmary.com/api#/paths/~1contacts/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Filter contacts by exact email address. |
| `offset` | query | `number` | no | Offset for paging through contacts in blocks of up to 1000. |
