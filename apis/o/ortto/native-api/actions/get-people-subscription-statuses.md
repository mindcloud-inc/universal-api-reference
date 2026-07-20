# Get People Subscription Statuses with Ortto

## Endpoint

- **Method:** `POST`
- **Path:** `/person/subscriptions`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [Get People Subscription Statuses](https://help.ortto.com/a-259-retrieve-peoples-subscription-statuses-subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `people[]` | body | `array<object>` | yes | People to check subscription statuses for. Each item can include email or person_id. |
| `audience_id` | body | `string` | no | Specific audience ID to check when retrieving audience subscription status. |
| `subscription` | body | `string` | no | Subscription type to inspect, such as email or sms. |
