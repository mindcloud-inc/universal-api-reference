# Get Issue Field Detail with Leiga

Retrieves issue field details from Leiga.

## Endpoint

- **Method:** `GET`
- **Path:** `/issue/issue-field-info`
- **Base URL:** `https://app.leiga.com/openapi/api`
- **Official documentation:** [Get Issue Field Detail](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741836.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issueTypeId` | query | `number` | yes | Issue Type ID |
| `projectId` | query | `number` | yes | Project ID |
| `fieldCode` | query | `string` | yes | Field Code |
