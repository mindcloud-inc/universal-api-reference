# Create Records with Zoho Recruit

Creates new records in a Zoho Recruit module.

## Endpoint

- **Method:** `POST`
- **Path:** `/:moduleApiName`
- **Base URL:** `https://recruit.zoho.com/recruit/v2`
- **Official documentation:** [Create Records](https://www.zoho.com/recruit/developer-guide/apiv2/insert-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleApiName` | path | `string` | yes | The Zoho Recruit module API name where the new records should be created. |
| `data` | body | `list<object>` | yes | An array of record objects to create. |
| `trigger` | body | `list<string>` | no | Automation triggers to run after record creation. |
| `$approved` | body | `boolean` | no | Create the records in approval mode when true. |
| `$state` | body | `string` | no | Create the records as draft or save state. Accepted values: `draft`, `save`. |
