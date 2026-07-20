# Create Webhook with Fibery

Creates a new webhook in Fibery.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/v2`
- **Base URL:** `https://{account}.fibery.io/api`
- **Official documentation:** [Create Webhook](https://the.fibery.io/@public/User_Guide/Guide/Webhooks-258)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Destination URL that should receive Fibery webhook events. |
| `type` | body | `string` | yes | Fibery type/database name to subscribe to, such as Space/Database. |
