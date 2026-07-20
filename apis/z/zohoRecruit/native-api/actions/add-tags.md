# Add Tags with Zoho Recruit

Adds tags to a Zoho Recruit record.

## Endpoint

- **Method:** `POST`
- **Path:** `/:moduleApiName/:recordId/actions/add_tags`
- **Base URL:** `https://recruit.zoho.com/recruit/v2`
- **Official documentation:** [Add Tags](https://www.zoho.com/recruit/developer-guide/apiv2/add-tags.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleApiName` | path | `string` | yes | The Zoho Recruit module API name that contains the record. |
| `recordId` | path | `string` | yes | The unique ID of the Zoho Recruit record. |
| `tag_names` | query | `string` | yes | Tag names to add to the record. Send multiple values as a string separated by `,`. |
| `data` | body | `list<object>` | no | Optional tag objects to create while adding tags, for example [{"name":"codex-quality-test","color_code":"#969696"}]. |
