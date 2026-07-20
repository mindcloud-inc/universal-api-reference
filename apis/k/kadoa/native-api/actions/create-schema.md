# Create Schema with Kadoa

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/schemas/`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Create Schema](https://docs.kadoa.com/api-reference/schemas/create-schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity` | body | `string` | no | Entity type |
| `fields` | body | `list<object>` | yes | JSON array of field defs |
| `name` | body | `string` | yes | Schema name |
