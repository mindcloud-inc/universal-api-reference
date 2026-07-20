# Add Subscriber User Data with Marketing Master IO

Adds user data to a Messenger subscriber in Marketing Master IO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messenger/subscriber/:subscriber_id/user_data/:variable_key`
- **Base URL:** `https://api.marketingmaster.io`
- **Official documentation:** [Add Subscriber User Data](https://developers.marketingmaster.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriber_id` | path | `string` | yes | — |
| `value` | body | `string` | yes | Value to store for the subscriber custom variable. |
| `variable_key` | path | `string` | yes | — |
