# Update Records with Zoho Recruit

Updates records in a Zoho Recruit module.

## Endpoint

- **Method:** `PUT`
- **Path:** `/:moduleApiName`
- **Base URL:** `https://recruit.zoho.com/recruit/v2`
- **Official documentation:** [Update Records](https://www.zoho.com/recruit/developer-guide/apiv2/update-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleApiName` | path | `string` | yes | The Zoho Recruit module API name where the records should be updated. |
| `data` | body | `list<object>` | yes | An array of record objects to update. |
| `trigger` | body | `list<string>` | no | Automation triggers to run after record update. |
| `$approved` | body | `boolean` | no | Update the records in approval mode when true. |
| `$state` | body | `string` | no | Update the records as draft or save state. Accepted values: `draft`, `save`. |
