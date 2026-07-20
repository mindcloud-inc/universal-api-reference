# Create Issue with Leiga

Creates a new issue in Leiga.

## Endpoint

- **Method:** `POST`
- **Path:** `/issue/add`
- **Base URL:** `https://app.leiga.com/openapi/api`
- **Official documentation:** [Create Issue](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741833.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issueTypeId` | body | `number` | yes | Issue Type ID |
| `data` | body | `object` | yes | Issue Field Values |
| `projectId` | body | `number` | yes | Project ID |
