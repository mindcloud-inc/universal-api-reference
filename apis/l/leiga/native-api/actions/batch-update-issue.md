# Batch Update Issue with Leiga

Updates multiple existing issues in Leiga.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/issue/batch-update`
- **Base URL:** `https://app.leiga.com/openapi/api`
- **Official documentation:** [Batch Update Issue](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-4700178.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issueTypeId` | body | `number` | yes | Issue Type ID |
| `data` | body | `object` | yes | Issues Field Values |
| `issueIds[]` | body | `array<number>` | yes | Issue IDs |
| `projectId` | body | `number` | yes | Project ID |
