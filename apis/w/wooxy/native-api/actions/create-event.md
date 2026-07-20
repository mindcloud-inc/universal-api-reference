# Create Event with Wooxy

Creates a new event in Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/custom-event/create`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Create Event](https://wooxy.com/api-documentation/events/create-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The unique event name. Use only letters and numbers, up to 40 characters. |
| `description` | body | `string` | no | Optional description for the event. |
| `isConversion` | body | `boolean` | no | Whether Wooxy should treat the event as a conversion. |
| `cost.value` | body | `number` | no | Optional event cost value. |
| `cost.currency` | body | `string` | no | Optional event cost currency (USD or EUR). |
