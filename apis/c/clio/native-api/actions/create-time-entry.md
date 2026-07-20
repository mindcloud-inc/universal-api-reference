# Create Time Entry with Clio Manage

Creates a new time entry in Clio Manage.

## Endpoint

- **Method:** `POST`
- **Path:** `/activities.json`
- **Base URL:** `https://app.clio.com/api/v4`
- **Official documentation:** [Create Time Entry](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Activities/operation/Activity%23create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.date` | body | `date` | yes |
| `data.matter.id` | body | `number` | no |
| `data.note` | body | `string` | no |
| `data.quantity` | body | `number` | no |
