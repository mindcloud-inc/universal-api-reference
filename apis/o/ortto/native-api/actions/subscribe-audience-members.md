# Subscribe Audience Members with Ortto

## Endpoint

- **Method:** `PUT`
- **Path:** `/audience/subscribe`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [Subscribe Audience Members](https://help.ortto.com/a-269-subscribe-or-unsubscribe-people-to-from-an-audience-subscribe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience_id` | body | `string` | yes | Audience to subscribe people to. |
| `people[]` | body | `array<object>` | yes | Audience member updates. |
| `async` | body | `boolean` | no | Queue the subscription update asynchronously. |
