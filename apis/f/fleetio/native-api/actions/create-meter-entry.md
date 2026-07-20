# Create Meter Entry with Fleetio

Creates a new meter entry in Fleetio.

## Endpoint

- **Method:** `POST`
- **Path:** `meter_entries`
- **Base URL:** `https://secure.fleetio.com/api/`
- **Official documentation:** [Create Meter Entry](https://developer.fleetio.com/docs/api/meter-entries-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vehicle_id` | body | `number` | yes | — |
| `value` | body | `number` | yes | The value of the meter. The unit can be configured at the `Account` level, or overridden at the `Vehicle` level. |
| `date` | body | `date` | yes | Meter Entries must follow the correct sequence, incrementing in value by date. For each entry, Fleetio validates to ensure that the value falls between any entries logged before and/or after. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `void` | body | `boolean` | no | Whether to mark this Meter Entry void or not.  See [Voiding Meter Entries](https://help.fleetio.com/s/article/Meter-Entry-Mark-As-Void-Unmark-As-Void). |
| `meter_type` | body | `string` | no | If this is a secondary meter reading, use this field.  If the vehicle's secondary meter is disabled, secondary meter values will be hidden in the web and mobile views until enabled. |
