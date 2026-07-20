# Mark Charge As Failed with OPN

Marks an existing charge as failed in OPN.

## Endpoint

- **Method:** `POST`
- **Path:** `/charges/:id/mark_as_failed`
- **Base URL:** `https://api.omise.co`
- **Official documentation:** [Mark Charge As Failed](https://docs.omise.co/charge-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The charge ID to mark as failed. |
