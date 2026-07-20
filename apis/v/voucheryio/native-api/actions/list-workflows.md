# List Workflows with Vouchery.io

## Endpoint

- **Method:** `GET`
- **Path:** `/workflows`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [List Workflows](https://docs.vouchery.io/reference/getapiv21workflows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | query | `number` | no | Campaign ID |
| `namespace` | query | `string` | no | Namespace |
| `page` | query | `number` | no | Result page (indexed from 1) |
| `per_page` | query | `number` | no | Results per page |
