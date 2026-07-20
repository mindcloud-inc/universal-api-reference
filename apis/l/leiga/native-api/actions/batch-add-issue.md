# Batch Add Issue with Leiga

Creates multiple new issues in Leiga.

## Endpoint

- **Method:** `POST`
- **Path:** `/issue/batch-add`
- **Base URL:** `https://app.leiga.com/openapi/api`
- **Official documentation:** [Batch Add Issue](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-4700177.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issueTypeId` | body | `number` | yes | Issue Type ID |
| `datas[]` | body | `array<object>` | yes | Issues Field Values |
| `projectId` | body | `number` | yes | Project ID |
