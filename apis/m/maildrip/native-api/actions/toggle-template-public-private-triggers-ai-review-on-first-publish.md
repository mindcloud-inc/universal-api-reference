# Toggle template public/private (triggers AI review on first publish) with Maildrip

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/templates/{templateId}/visibility`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Toggle template public/private (triggers AI review on first publish)](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `templateId` | path | `string` | yes |
| `isPublic` | body | `boolean` | no |
