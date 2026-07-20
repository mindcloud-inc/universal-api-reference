# Retrieve Job By D.O. Number with Detrack

Retrieves a job from Detrack by D.O. number.

## Endpoint

- **Method:** `GET`
- **Path:** `/dn/jobs/:do_number`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [Retrieve Job By D.O. Number](https://detrackapiv2.docs.apiary.io/#reference/jobs/retrieve-update-delete-by-do/retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `do_number` | path | `string` | yes | Job D.O. number. |
| `type` | query | `string` | no | Optional job type: Delivery or Collection. |
