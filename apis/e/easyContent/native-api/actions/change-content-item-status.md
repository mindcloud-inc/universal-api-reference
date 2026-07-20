# Change Content Item Status with EasyContent

Updates a content item's workflow status in EasyContent.

## Endpoint

- **Method:** `POST`
- **Path:** `/zapier/actions/create/change_item_status`
- **Base URL:** `https://easycontent.io/api`
- **Official documentation:** [Change Content Item Status](https://easycontent.io/content-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | body | `number` | yes |
| `articleId` | body | `number` | yes |
| `newStatusId` | body | `number` | yes |
