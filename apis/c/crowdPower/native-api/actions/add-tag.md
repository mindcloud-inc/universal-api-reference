# Add Tag with CrowdPower

Adds a tag to a customer in CrowdPower.

## Endpoint

- **Method:** `POST`
- **Path:** `customers/:customer_id/tags`
- **Base URL:** `https://api.crowdpower.io/v1`
- **Official documentation:** [Add Tag](https://documenter.getpostman.com/view/17896162/UV5TFKbh)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | Customer identifier. |
| `name` | body | `string` | yes | Tag name to add. |
