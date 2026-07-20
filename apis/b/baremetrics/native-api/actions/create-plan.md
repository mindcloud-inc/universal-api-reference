# Create Plan with Baremetrics

Creates a plan in Baremetrics.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/:source_id/plans`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [Create Plan](https://developers.baremetrics.com/reference/create-plan)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_id` | path | `string` | yes | Please see [Sources](ref:sources) |
| `oid` | body | `string` | yes | Your unique ID for the plan |
| `name` | body | `string` | yes | Your internal name for this plan. This will be displayed in the Plan Breakout section |
| `currency` | body | `string` | yes | The ISO code of the currency of this plan. E.G: usd |
| `amount` | body | `number` | yes | How much is this plan? (In cents) |
| `interval` | body | `string` | yes | day, month or year |
| `interval_count` | body | `number` | yes | — |
| `trial_duration` | body | `number` | no | The duration of this trial. This is to be used in conjunction with trial_duration_unit |
| `trial_duration_unit` | body | `string` | no | This is to be used in conjunction with trial_duration |
