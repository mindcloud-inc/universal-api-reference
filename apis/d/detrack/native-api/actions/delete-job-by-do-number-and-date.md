# Delete Job By D.O. Number And Date with Detrack

Deletes an existing job from Detrack by D.O. number and date.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/dn/jobs/:do_number/:date`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [Delete Job By D.O. Number And Date](https://detrackapiv2.docs.apiary.io/#reference/jobs/retrieve-update-delete-by-do-and-date/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `do_number` | path | `string` | yes | Job D.O. number. |
| `date` | path | `string` | yes | Job date in YYYY-MM-DD format. |
| `type` | query | `string` | no | Optional job type: Delivery or Collection. |
