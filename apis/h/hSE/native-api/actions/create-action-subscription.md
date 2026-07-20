# Create Action Subscription with 4HSE

Creates a new action subscription in 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/action-subscription/create`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [Create Action Subscription](https://docs.4hse.com/en/api/actionsubscription/#operation-createActionSubscription-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action_id` | body | `string` | yes | The preventive action this resource is subscribed to. |
| `subscriber_id` | body | `string` | yes | The ID of the subscribed resource. |
| `subscriber_type` | body | `string` | yes | The type of subscribed resource. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. |
| `data` | body | `object` | no | Additional structured data in JSON format. |
| `subtenant_id` | body | `string` | yes | The office of this subscription. |
| `tenant_id` | body | `string` | yes | The project of this subscription. |
