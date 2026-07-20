# Update Campaign Status with SmartReach

Updates campaign status in SmartReach.

## Endpoint

- **Method:** `PUT`
- **Path:** `/campaigns/:campaign_id/status`
- **Base URL:** `https://api.smartreach.io/api/v3`
- **Official documentation:** [Update Campaign Status](https://help.smartreach.io/reference/startstopcampaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | ID of campaign |
| `status` | body | `string` | yes | Status of campaign can be changed to 'running', 'scheduled', 'stopped'. |
| `schedule_start_at` | body | `number` | no | Required for scheduling a campaign for a specific date. The date-time with respective time-zone of schedule start should be converted to Epoch milliseconds and passed. |
