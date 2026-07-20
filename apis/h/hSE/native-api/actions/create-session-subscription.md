# Create Session Subscription with 4HSE

Creates a new session subscription in 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/action-session-subscription/create`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [Create Session Subscription](https://docs.4hse.com/en/api/actionsessionsubscription/#operation-createActionSessionSubscription-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action_session_id` | body | `string` | yes | The session the resource is enrolled in. |
| `action_subscription_id` | body | `string` | yes | The compliance schedule entry linked to this enrollment. |
| `data` | body | `object` | no | Additional structured data in JSON format. |
| `subtenant_id` | body | `string` | yes | The office of this enrollment. |
| `tenant_id` | body | `string` | yes | The project of this enrollment. |
| `done` | body | `number` | no | Session outcome for this enrollee. Accepted values: `0`, `1`, `2`. |
| `warning` | body | `number` | no | Warning flag for this enrollment. Accepted values: `0`, `1`. |
| `certificate_id` | body | `string` | no | Certificate generated from this session for this enrollee. |
| `date_begin` | body | `date` | no | Start date of validity for this enrollment. |
| `date_expire` | body | `date` | no | Expiration date for this enrollment. |
