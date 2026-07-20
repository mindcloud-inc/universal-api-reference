# Update Action Subscription with 4HSE

Updates an existing action subscription in 4HSE.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/action-subscription/update/:id`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [Update Action Subscription](https://docs.4hse.com/en/api/actionsubscription/#operation-updateActionSubscription-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The action subscription to update. |
| `action_id` | body | `string` | yes | The preventive action this resource is subscribed to. |
| `subscriber_id` | body | `string` | yes | The ID of the subscribed resource. |
| `subscriber_type` | body | `string` | yes | The type of subscribed resource. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. |
| `data` | body | `object` | no | Additional structured data in JSON format. |
| `subtenant_id` | body | `string` | yes | The office of this subscription. |
| `tenant_id` | body | `string` | yes | The project of this subscription. |
