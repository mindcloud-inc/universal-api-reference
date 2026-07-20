# Create Loop with HITL Platform

## Endpoint

- **Method:** `POST`
- **Path:** `/api/loops`
- **Base URL:** `https://api.hitl.sh/v1`
- **Official documentation:** [Create Loop](https://docs.hitl.sh/api-reference/loops/create-loop)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Description shown to loop members. |
| `icon` | body | `string` | no | Icon name for the loop. |
| `name` | body | `string` | yes | Name of the loop to create. |
