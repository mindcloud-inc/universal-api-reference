# Get Organization with Microsoft Entra

## Endpoint

- **Method:** `GET`
- **Path:** `/organization/:organizationId`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [Get Organization](https://learn.microsoft.com/en-us/graph/api/organization-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$select` | query | `string` | no | Comma-separated organization properties to return. |
| `organizationId` | path | `list<string>` | yes | — |
