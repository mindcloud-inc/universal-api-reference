# Put Subscription On Hold with Billwerkplus

Puts a subscription on hold in Billwerkplus.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscription/:handle/on_hold`
- **Base URL:** `https://api.frisbii.com/v1`
- **Official documentation:** [Put Subscription On Hold](https://docs.frisbii.com/reference/onhold)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `handle` | path | `string` | yes | Subscription handle. |
| `compensation_method` | body | `string` | no | Compensation method for the current partial period. |
