# Get User Account Analytics with Pinterest

Retrieves analytics for the current Pinterest user account.

## Endpoint

- **Method:** `GET`
- **Path:** `user_account/analytics`
- **Base URL:** `https://api.pinterest.com/v5`
- **Official documentation:** [Get User Account Analytics](https://developers.pinterest.com/docs/api/v5/#operation/user_account/analytics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | yes | — |
| `end_date` | query | `string` | yes | — |
| `metric_types` | query | `list<string>` | no | Accepted values: `ENGAGEMENT`, `ENGAGEMENT_RATE`, `IMPRESSION`, `OUTBOUND_CLICK`, `OUTBOUND_CLICK_RATE`, `PIN_CLICK`, `PIN_CLICK_RATE`, `SAVE`, `SAVE_RATE`. Send multiple values as a string separated by `,`. |
