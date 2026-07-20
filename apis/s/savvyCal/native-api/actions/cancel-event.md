# Cancel Event with SavvyCal

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/events/:event_id/cancel`
- **Base URL:** `https://api.savvycal.com`
- **Official documentation:** [Cancel Event](https://developers.savvycal.com/api/cancel-event)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `event_id` | path | `string` | yes |
| `cancel_reason` | body | `string` | no |
