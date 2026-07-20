# Update Document Party with fynk

Updates a document party in fynk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/documents/:document/parties/:party`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Update Document Party](https://app.fynk.com/v1/docs#/operations/v1.documents.parties.update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | path | `string` | no | Document UUID. |
| `entity_name` | body | `string` | no | Updated party entity name. |
| `party` | path | `string` | no | Party UUID. |
