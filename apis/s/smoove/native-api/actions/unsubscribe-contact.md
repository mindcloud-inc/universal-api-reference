# Unsubscribe Contact with Smoove

Unsubscribes a contact from Smoove campaigns and lists.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/Contacts/:id/Unsubscribe`
- **Base URL:** `https://rest.smoove.io`
- **Official documentation:** [Unsubscribe Contact](https://rest.smoove.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `by` | query | `list` | yes | Accepted values: `CellPhone`, `ContactId`, `Email`, `ExternalId`. |
| `reason` | body | `string` | no | — |
