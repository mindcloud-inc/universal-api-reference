# Create Job with Detrack

Creates a new job in Detrack.

## Endpoint

- **Method:** `POST`
- **Path:** `/dn/jobs`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [Create Job](https://detrackapiv2.docs.apiary.io/#reference/jobs/list-create/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.do_number` | body | `string` | yes | Unique delivery order number for the job. |
| `data.date` | body | `string` | yes | Job date in YYYY-MM-DD format. |
| `data.address` | body | `string` | yes | Delivery address. |
| `data.deliver_to_collect_from` | body | `string` | no | Recipient or contact name. |
