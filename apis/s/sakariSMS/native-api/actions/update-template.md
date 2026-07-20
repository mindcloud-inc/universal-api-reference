# Update Template with Sakari SMS

Updates an existing template in Sakari SMS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/accounts/:accountId/templates/:templateId`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [Update Template](https://developer.sakari.io/api-reference/templates/updates-a-template)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `templateId` | path | `string` | yes |
| `name` | body | `string` | no |
| `template` | body | `string` | no |
| `type` | body | `string` | no |
