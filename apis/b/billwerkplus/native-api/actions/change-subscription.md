# Change Subscription with Billwerkplus

Updates a subscription plan or quantity in Billwerkplus.

## Endpoint

- **Method:** `PUT`
- **Path:** `/subscription/:handle`
- **Base URL:** `https://api.frisbii.com/v1`
- **Official documentation:** [Change Subscription](https://docs.frisbii.com/reference/changesubscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `handle` | path | `string` | yes | Subscription handle. |
| `timing` | body | `string` | yes | When to perform the change. |
| `plan` | body | `string` | no | Plan handle to change to. |
| `quantity` | body | `number` | no | Updated subscription quantity. |
