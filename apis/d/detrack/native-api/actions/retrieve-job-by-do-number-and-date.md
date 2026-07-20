# Retrieve Job By D.O. Number And Date with Detrack

Retrieves a job from Detrack by D.O. number and date.

## Endpoint

- **Method:** `GET`
- **Path:** `/dn/jobs/:do_number/:date`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [Retrieve Job By D.O. Number And Date](https://detrackapiv2.docs.apiary.io/#reference/jobs/retrieve-update-delete-by-do-and-date/retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `do_number` | path | `string` | yes | Job D.O. number. |
| `date` | path | `string` | yes | Job date in YYYY-MM-DD format. |
| `type` | query | `string` | no | Optional job type: Delivery or Collection. |
