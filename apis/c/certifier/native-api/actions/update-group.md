# Update Group with Certifier

Updates an existing group in Certifier.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/groups/:id`
- **Base URL:** `https://api.certifier.io/v1`
- **Official documentation:** [Update Group](https://developers.certifier.io/docs/api-reference/groups/update-a-group)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
| `certificateDesignId` | body | `string` | no |
| `badgeDesignId` | body | `string` | no |
| `learningEventUrl` | body | `string` | no |
