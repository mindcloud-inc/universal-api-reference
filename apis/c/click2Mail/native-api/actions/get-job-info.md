# Get Job Info with Click2Mail

Retrieves detailed job information from Click2Mail.

## Endpoint

- **Method:** `GET`
- **Path:** `/molpro/jobs/info/{id}`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Get Job Info](https://developers.click2mail.com/reference/getjobinfo)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | job id |
| `mappingHeadings` | query | `string` | no | column headings used in the address mapping |
