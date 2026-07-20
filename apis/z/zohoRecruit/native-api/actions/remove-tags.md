# Remove Tags with Zoho Recruit

Removes tags from a Zoho Recruit record.

## Endpoint

- **Method:** `POST`
- **Path:** `/:moduleApiName/:recordId/actions/remove_tags`
- **Base URL:** `https://recruit.zoho.com/recruit/v2`
- **Official documentation:** [Remove Tags](https://www.zoho.com/recruit/developer-guide/apiv2/remove-tags.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleApiName` | path | `string` | yes | The Zoho Recruit module API name that contains the record. |
| `recordId` | path | `string` | yes | The unique ID of the Zoho Recruit record. |
| `tag_names` | query | `string` | yes | Tag names to remove from the record. Send multiple values as a string separated by `,`. |
