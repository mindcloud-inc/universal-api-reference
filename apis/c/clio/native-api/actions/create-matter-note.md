# Create Matter Note with Clio Manage

Creates a new matter note in Clio Manage.

## Endpoint

- **Method:** `POST`
- **Path:** `/notes.json`
- **Base URL:** `https://app.clio.com/api/v4`
- **Official documentation:** [Create Matter Note](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Notes/operation/Note%23create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.matter.id` | body | `number` | yes |
| `data.contact.id` | body | `number` | yes |
| `data.subject` | body | `string` | no |
| `data.detail` | body | `string` | no |
