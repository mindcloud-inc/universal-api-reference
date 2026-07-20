# Check Contact Exists with Smoove

Checks whether a contact exists in Smoove.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/Contacts/:id/Exists`
- **Base URL:** `https://rest.smoove.io`
- **Official documentation:** [Check Contact Exists](https://rest.smoove.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `by` | query | `list` | yes | Accepted values: `CellPhone`, `ContactId`, `Email`, `ExternalId`. |
