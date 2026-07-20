# Add Notes with CrowdPower

Updates customer notes in CrowdPower.

## Endpoint

- **Method:** `PUT`
- **Path:** `customers/:customer_id/notes`
- **Base URL:** `https://api.crowdpower.io/v1`
- **Official documentation:** [Add Notes](https://documenter.getpostman.com/view/17896162/UV5TFKbh)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | Customer identifier. |
| `notes` | body | `string` | yes | Notes to append to the customer. |
