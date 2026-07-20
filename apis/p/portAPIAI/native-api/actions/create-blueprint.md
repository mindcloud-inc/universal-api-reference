# Create Blueprint with Port API AI

Creates a blueprint in Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/blueprints`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Create Blueprint](https://docs.port.io/api-reference/create-a-blueprint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `icon` | body | `string` | yes | Blueprint icon |
| `identifier` | body | `string` | yes | Blueprint identifier |
| `schema` | body | `object` | yes | Blueprint schema |
| `title` | body | `string` | yes | Blueprint title |
