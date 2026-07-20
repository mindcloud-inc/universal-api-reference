# Track Subscriber Event with PushAlert

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/web-push/track/event`
- **Base URL:** `https://api.pushalert.co`
- **Official documentation:** [Track Subscriber Event](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-custom-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriber` | body | `string` | yes | Subscriber ID that triggered the event. |
| `eventCategory` | body | `string` | yes | Object or page that was interacted with. |
| `eventAction` | body | `string` | yes | Type of interaction. |
| `eventLabel` | body | `string` | no | Optional label for categorizing the event. |
| `eventValue` | body | `string` | no | Optional numeric value associated with the event. |
