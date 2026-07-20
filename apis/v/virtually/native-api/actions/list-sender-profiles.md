# List Sender Profiles with Virtually

Retrieves sender profiles for a platform from Virtually.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/orgs/:orgId/members/senderProfiles/:platformName`
- **Base URL:** `https://app.tryvirtually.com`
- **Official documentation:** [List Sender Profiles](https://app.tryvirtually.com/api/docs#/Members/MembersController_getSenderProfiles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `platformName` | path | `string` | yes | The platform name. |
