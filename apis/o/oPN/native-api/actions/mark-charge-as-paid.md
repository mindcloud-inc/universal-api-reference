# Mark Charge As Paid with OPN

Marks an existing charge as paid in OPN.

## Endpoint

- **Method:** `POST`
- **Path:** `/charges/:id/mark_as_paid`
- **Base URL:** `https://api.omise.co`
- **Official documentation:** [Mark Charge As Paid](https://docs.omise.co/charge-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The charge ID to mark as paid. |
