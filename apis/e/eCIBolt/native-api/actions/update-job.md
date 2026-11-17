# Update Job with ECI Bolt

## Endpoint

- **Method:** `PATCH`
- **Path:** `/open/v1/jobs/:id`
- **Base URL:** `https://app.bolttech.net`
- **Official documentation:** [Update Job](https://app.bolttech.net/api-docs/index.html#/Jobs/patch_open_v1_jobs__id_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Id of the job. |
| `job` | body | `object` | no | — |
| `job.address` | body | `string` | no | Maximum length: 255. |
| `job.lot` | body | `string` | no | — |
| `job.block` | body | `string` | no | — |
| `job.active` | body | `boolean` | no | — |
| `job.permit_number` | body | `string` | no | — |
| `job.permit_date` | body | `date` | no | Bolt expects this date as MM/DD/YYYY. |
| `job.start_date` | body | `date` | no | Bolt expects this date as MM/DD/YYYY. |
| `job.builder_job_number` | body | `string` | no | — |
| `job.notes` | body | `string` | no | — |
| `job.zip` | body | `string` | no | — |
| `job.accounting_number` | body | `string` | no | — |
| `job.under_warranty` | body | `boolean` | no | — |
| `job.municipality` | body | `string` | no | — |
| `job.job_type_id` | body | `number` | no | — |
| `job.skip_address_uniqueness` | body | `boolean` | no | — |
| `job.floorplan_id` | body | `number` | no | — |
| `job.close_date` | body | `date` | no | Bolt expects this date as MM/DD/YYYY. |
| `job.square_footage` | body | `number` | no | — |
| `etag` | body | `string` | yes | Use the etag returned by a fresh Get request to avoid overwriting a newer record. |
