# Search Issues with Leiga

Finds issues in Leiga using paginated project filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/issue/page`
- **Base URL:** `https://app.leiga.com/openapi/api`
- **Official documentation:** [Search Issues](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741839.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | body | `number` | yes | Project ID |
