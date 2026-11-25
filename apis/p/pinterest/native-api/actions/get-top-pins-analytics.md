# Get Top Pins Analytics with Pinterest

Retrieves top pin analytics from Pinterest.

## Endpoint

- **Method:** `GET`
- **Path:** `user_account/analytics/top_pins`
- **Base URL:** `https://api.pinterest.com/v5`
- **Official documentation:** [Get Top Pins Analytics](https://developers.pinterest.com/docs/api/v5/#operation/user_account/analytics/top_pins)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | yes | — |
| `end_date` | query | `string` | yes | — |
| `sort_by` | query | `list<string>` | yes | Accepted values: `ENGAGEMENT`, `IMPRESSION`, `OUTBOUND_CLICK`, `PIN_CLICK`, `SAVE`. |
| `metric_types` | query | `list<string>` | no | Accepted values: `ENGAGEMENT`, `ENGAGEMENT_RATE`, `IMPRESSION`, `OUTBOUND_CLICK`, `OUTBOUND_CLICK_RATE`, `PIN_CLICK`, `PIN_CLICK_RATE`, `SAVE`, `SAVE_RATE`. Send multiple values as a string separated by `,`. |
