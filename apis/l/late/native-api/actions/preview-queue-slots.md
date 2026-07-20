# Preview Queue Slots with Late

## Endpoint

- **Method:** `GET`
- **Path:** `/queue/preview`
- **Base URL:** `https://zernio.com/api/v1`
- **Official documentation:** [Preview Queue Slots](https://docs.zernio.com/queue/preview-upcoming-slots)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `profileId` | query | `string` | yes |
| `queueId` | query | `string` | no |
| `count` | query | `number` | no |
