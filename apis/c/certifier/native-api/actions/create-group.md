# Create Group with Certifier

Creates a new group in Certifier.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups`
- **Base URL:** `https://api.certifier.io/v1`
- **Official documentation:** [Create Group](https://developers.certifier.io/docs/api-reference/groups/create-a-group)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `certificateDesignId` | body | `string` | no |
| `badgeDesignId` | body | `string` | no |
| `learningEventUrl` | body | `string` | no |
