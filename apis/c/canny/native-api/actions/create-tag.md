# Create Tag with Canny

Creates a new tag in Canny.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tags/create`
- **Base URL:** `https://canny.io/api`
- **Official documentation:** [Create Tag](https://developers.canny.io/api-reference#create_tag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `boardID` | body | `string` | yes |
| `name` | body | `string` | yes |
