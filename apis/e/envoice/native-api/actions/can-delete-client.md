# Can Delete Client with Envoice

Checks whether a client can be deleted in Envoice.

## Endpoint

- **Method:** `GET`
- **Path:** `client/candelete`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Can Delete Client](https://www.envoice.in/reference/api/docs/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | yes | Client identifier to check for deletion. |
