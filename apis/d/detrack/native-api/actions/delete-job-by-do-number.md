# Delete Job By D.O. Number with Detrack

Deletes an existing job from Detrack by D.O. number.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/dn/jobs/:do_number`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [Delete Job By D.O. Number](https://detrackapiv2.docs.apiary.io/#reference/jobs/retrieve-update-delete-by-do/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `do_number` | path | `string` | yes | Job D.O. number. |
| `type` | query | `string` | no | Optional job type: Delivery or Collection. |
