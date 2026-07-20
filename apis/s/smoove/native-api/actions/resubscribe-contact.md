# Resubscribe Contact with Smoove

Resubscribes a contact to Smoove campaigns and lists.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/Contacts/:id/Resubscribe`
- **Base URL:** `https://rest.smoove.io`
- **Official documentation:** [Resubscribe Contact](https://rest.smoove.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `by` | query | `list` | no | Accepted values: `CellPhone`, `ContactId`, `Email`, `ExternalId`. |
