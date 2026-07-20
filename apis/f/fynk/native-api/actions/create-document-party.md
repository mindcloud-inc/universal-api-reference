# Create Document Party with fynk

Creates a document party in fynk.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/:document/parties`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Create Document Party](https://app.fynk.com/v1/docs#/operations/v1.documents.parties.store)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | path | `string` | no | Document UUID. |
| `entity_name` | body | `string` | no | Party entity name. |
| `entity_type` | body | `string` | no | Party entity type. |
| `reference` | body | `string` | no | Party reference label. |
| `scope` | body | `string` | no | Party scope. |
