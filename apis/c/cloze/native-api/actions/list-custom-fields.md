# List Custom Fields with Cloze

Retrieves custom fields from Cloze.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/user/fields`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [List Custom Fields](https://api.cloze.com/api-docs/#/paths/v1-user-fields/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `relationtype` | query | `list<string>` | no | Filter custom fields by relation type: person, project, or company. Accepted values: `company`, `person`, `project`. |
