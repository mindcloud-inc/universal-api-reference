# List Jobs with Click2Mail

Retrieves a list of jobs from Click2Mail.

## Endpoint

- **Method:** `GET`
- **Path:** `/molpro/jobs`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [List Jobs](https://developers.click2mail.com/reference/getjobs_1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `string` | yes | start date in yyyy-MM-dd format |
| `endDate` | query | `string` | no | end date in yyyy-MM-dd format |
| `mailClass` | query | `string` | no | mail class |
| `sku` | query | `string` | no | sku |
