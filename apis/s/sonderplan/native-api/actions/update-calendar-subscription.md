# Update Calendar Subscription with Sonderplan

## Endpoint

- **Method:** `PUT`
- **Path:** `/calendar-subscription/import`
- **Base URL:** `https://api.sonderplan.com/v2`
- **Official documentation:** [Update Calendar Subscription](https://docs.sonderplan.com/api-reference/calendar-subscription/update-calendar-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Calendar subscription payload. |
| `id` | query | `string` | yes | Calendar subscription ID. |
