# Add Issue Relation with Leiga

Creates an issue relation in Leiga.

## Endpoint

- **Method:** `POST`
- **Path:** `/issue/add-relationship`
- **Base URL:** `https://app.leiga.com/openapi/api`
- **Official documentation:** [Add Issue Relation](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741849.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issueId` | body | `number` | yes | Issue ID |
| `linkedIssueId` | body | `number` | yes | Related Issue ID |
| `type` | body | `string` | yes | Relation Type |
