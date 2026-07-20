# Create Activity Description with Clio Manage

Creates a new activity description in Clio Manage.

## Endpoint

- **Method:** `POST`
- **Path:** `/activity_descriptions.json`
- **Base URL:** `https://app.clio.com/api/v4`
- **Official documentation:** [Create Activity Description](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Activity%20Descriptions/operation/ActivityDescription%23create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.name` | body | `string` | yes | Detailed description name. |
| `data.default` | body | `boolean` | no | Mark this as the default activity description. |
