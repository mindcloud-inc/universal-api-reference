# Remove Tag with CrowdPower

Removes a tag from a customer in CrowdPower.

## Endpoint

- **Method:** `DELETE`
- **Path:** `customers/:customer_id/tags`
- **Base URL:** `https://api.crowdpower.io/v1`
- **Official documentation:** [Remove Tag](https://documenter.getpostman.com/view/17896162/UV5TFKbh)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | Customer identifier. |
| `name` | body | `string` | yes | Tag name to remove. |
