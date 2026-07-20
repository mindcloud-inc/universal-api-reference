# Create Tag with NobelSMS

Creates a new tag in NobelSMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/tag`
- **Base URL:** `https://api.nobelsms.com/rest`
- **Official documentation:** [Create Tag](https://api.nobelsms.com/rest/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Tag name. |
| `type` | body | `number` | no | Tag type: 1 for contact tags, 2 for black list tags. |
