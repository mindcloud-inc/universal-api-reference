# Remove Subscriber User Data with Marketing Master IO

Removes user data from a Messenger subscriber in Marketing Master IO.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/messenger/subscriber/:subscriber_id/user_data/:variable_key`
- **Base URL:** `https://api.marketingmaster.io`
- **Official documentation:** [Remove Subscriber User Data](https://developers.marketingmaster.io/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `subscriber_id` | path | `string` | yes |
| `variable_key` | path | `string` | yes |
