# Update Campaign Status with LinkedCamp

## Endpoint

- **Method:** `PUT`
- **Path:** `/campaigns/:campaignId`
- **Base URL:** `https://api.linkedcamp.com`
- **Official documentation:** [Update Campaign Status](https://api.linkedcamp.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Campaign identifier. |
| `status` | query | `string` | yes | New campaign status: ACTIVE, PAUSED, COMPLETED, FAILED, or ARCHIVED. |
