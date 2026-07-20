# Update Job By D.O. Number with Detrack

Updates an existing job in Detrack by D.O. number.

## Endpoint

- **Method:** `PUT`
- **Path:** `/dn/jobs/:do_number`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [Update Job By D.O. Number](https://detrackapiv2.docs.apiary.io/#reference/jobs/retrieve-update-delete-by-do/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `do_number` | path | `string` | yes | Job D.O. number. |
| `data` | body | `object` | yes | Job fields to update, using the Detrack update body shape. |
| `type` | query | `string` | no | Optional job type: Delivery or Collection. |
