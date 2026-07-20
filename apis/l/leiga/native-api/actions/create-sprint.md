# Create Sprint with Leiga

Creates a new sprint in Leiga.

## Endpoint

- **Method:** `POST`
- **Path:** `/sprint/add`
- **Base URL:** `https://app.leiga.com/openapi/api`
- **Official documentation:** [Create Sprint](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741855.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Sprint Name |
| `projectId` | body | `number` | yes | Project ID |
