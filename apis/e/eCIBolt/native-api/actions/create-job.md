# Create Job with ECI Bolt

## Endpoint

- **Method:** `POST`
- **Path:** `/open/v1/jobs`
- **Base URL:** `https://app.bolttech.net`
- **Official documentation:** [Create Job](https://app.bolttech.net/api-docs/index.html#/Jobs/post_open_v1_jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job` | body | `object` | no | — |
| `job.address` | body | `string` | yes | Maximum length: 255. |
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
| `job.skip_address_uniqueness` | body | `boolean` | no | — |
| `job.floorplan_id` | body | `number` | no | — |
| `job.job_type_id` | body | `number` | no | — |
| `job.create_contractual_work_orders` | body | `boolean` | no | — |
| `job.not_known` | body | `boolean` | no | — |
| `job.builder_service` | body | `boolean` | no | — |
| `job.community_id` | body | `number` | no | — |
| `job.city_id` | body | `number` | no | — |
| `job.customer_id` | body | `number` | no | — |
| `job.supervisor_id` | body | `number` | no | — |
| `job.close_date` | body | `date` | no | Bolt expects this date as MM/DD/YYYY. |
| `job.square_footage` | body | `number` | no | — |
