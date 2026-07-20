# Change Next Renewal Date with Billwerkplus

Updates a subscription's next renewal date in Billwerkplus.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscription/:handle/change_next_period_start`
- **Base URL:** `https://api.frisbii.com/v1`
- **Official documentation:** [Change Next Renewal Date](https://docs.frisbii.com/reference/changenextperiodstartjson)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `handle` | path | `string` | yes | Subscription handle. |
| `next_period_start` | body | `string` | yes | Requested next period start date and time. |
