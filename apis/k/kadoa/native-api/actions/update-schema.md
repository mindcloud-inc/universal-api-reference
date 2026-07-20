# Update Schema with Kadoa

## Endpoint

- **Method:** `PUT`
- **Path:** `/v4/schemas/:schemaId`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Update Schema](https://docs.kadoa.com/api-reference/schemas/update-schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity` | body | `string` | no | Entity type |
| `fields` | body | `list<object>` | no | JSON array of field defs |
| `name` | body | `string` | no | Schema name |
| `schemaId` | path | `string` | yes | Schema ID |
