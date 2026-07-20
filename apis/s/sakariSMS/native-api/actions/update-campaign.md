# Update Campaign with Sakari SMS

Updates an existing campaign in Sakari SMS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/accounts/:accountId/campaigns/:campaignId`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [Update Campaign](https://developer.sakari.io/api-reference/campaigns/updates-a-campaign)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `campaignId` | path | `string` | yes |
| `name` | body | `string` | no |
| `trigger` | body | `object` | no |
| `trigger.code` | body | `string` | no |
| `template` | body | `string` | no |
| `reporting` | body | `object` | no |
| `reporting.when` | body | `string` | no |
