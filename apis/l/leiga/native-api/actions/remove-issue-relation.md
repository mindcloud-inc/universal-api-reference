# Remove Issue Relation with Leiga

Deletes an existing issue relation from Leiga.

## Endpoint

- **Method:** `POST`
- **Path:** `/issue/remove-relationship`
- **Base URL:** `https://app.leiga.com/openapi/api`
- **Official documentation:** [Remove Issue Relation](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741845.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issueId` | body | `number` | yes | Issue ID |
| `linkedIssueId` | body | `number` | yes | Related Issue ID |
| `type` | body | `string` | yes | Relation Type |
