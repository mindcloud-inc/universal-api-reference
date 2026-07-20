# List Export Jobs with Castor EDC

Retrieves export jobs from Castor EDC by study.

## Endpoint

- **Method:** `GET`
- **Path:** `/study/:study_id/export`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [List Export Jobs](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The ID of the study for which this call should be made |
| `page` | query | `number` | no | The page to retrieve |
| `page_size` | query | `number` | no | The size of pages |
