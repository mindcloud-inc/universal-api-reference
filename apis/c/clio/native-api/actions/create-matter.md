# Create Matter with Clio Manage

Creates a new matter in Clio Manage.

## Endpoint

- **Method:** `POST`
- **Path:** `/matters.json`
- **Base URL:** `https://app.clio.com/api/v4`
- **Official documentation:** [Create Matter](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Matters/operation/Matter%23create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.client.id` | body | `number` | yes |
| `data.description` | body | `string` | yes |
