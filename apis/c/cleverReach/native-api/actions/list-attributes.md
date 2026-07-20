# List Attributes with CleverReach

Retrieves local and global attributes from CleverReach.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/attributes.json`
- **Base URL:** `https://rest.cleverreach.com`
- **Official documentation:** [List Attributes](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/attributes-v3.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | query | `string` | no | ID of the group - leave empty for global attributes. |
