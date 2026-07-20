# Update Tag with NobelSMS

Updates an existing tag in NobelSMS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tag/:id`
- **Base URL:** `https://api.nobelsms.com/rest`
- **Official documentation:** [Update Tag](https://api.nobelsms.com/rest/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Tag ID. |
| `name` | body | `string` | yes | Tag name. |
| `type` | body | `number` | no | Tag type: 1 for contact tags, 2 for black list tags. |
