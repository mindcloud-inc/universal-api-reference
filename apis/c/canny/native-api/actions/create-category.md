# Create Category with Canny

Creates a new category in Canny.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/categories/create`
- **Base URL:** `https://canny.io/api`
- **Official documentation:** [Create Category](https://developers.canny.io/api-reference#create_category)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `boardID` | body | `string` | yes |
| `name` | body | `string` | yes |
| `parentID` | body | `string` | no |
| `subscribeAdmins` | body | `boolean` | yes |
