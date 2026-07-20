# Update Campaign with ManyReach

Updates an existing campaign in ManyReach.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://api.manyreach.com/api/v2/campaigns/:id`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [Update Campaign](https://api.manyreach.com/api#v2/tag/campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | HTML email body for the initial campaign message. |
| `description` | body | `string` | no | Campaign description. |
| `id` | path | `string` | yes | The ID of the campaign to update. |
| `name` | body | `string` | no | Campaign display name. |
| `subject` | body | `string` | no | Email subject line for the initial campaign email. |
