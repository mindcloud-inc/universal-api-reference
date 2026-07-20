# Update Event with Wooxy

Updates an existing event in Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/custom-event/update`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Update Event](https://wooxy.com/api-documentation/events/update-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customEvent` | body | `string` | yes | The existing event ID or event name. |
| `name` | body | `string` | yes | The new unique event name. Use only letters and numbers, up to 40 characters. |
| `description` | body | `string` | no | Optional updated description. |
| `isConversion` | body | `boolean` | no | Whether Wooxy should treat the event as a conversion. |
| `cost.value` | body | `number` | no | Optional updated cost value. |
| `cost.currency` | body | `string` | no | Optional updated cost currency (USD or EUR). |
