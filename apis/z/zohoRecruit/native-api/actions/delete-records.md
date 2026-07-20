# Delete Records with Zoho Recruit

Deletes records from a Zoho Recruit module.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/:moduleApiName`
- **Base URL:** `https://recruit.zoho.com/recruit/v2`
- **Official documentation:** [Delete Records](https://www.zoho.com/recruit/developer-guide/apiv2/delete-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleApiName` | path | `string` | yes | The Zoho Recruit module API name whose records you want to delete. |
| `ids` | query | `string` | yes | A comma-separated list of Zoho Recruit record IDs to delete. Send multiple values as a string separated by `,`. |
| `wf_trigger` | query | `boolean` | no | Whether to trigger workflows when the records are deleted. |
