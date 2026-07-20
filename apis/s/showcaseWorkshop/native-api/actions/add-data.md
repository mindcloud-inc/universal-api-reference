# Add Data with Showcase Workshop

Creates a data item in Showcase Workshop.

## Endpoint

- **Method:** `POST`
- **Path:** `/data/`
- **Base URL:** `https://app.showcaseworkshop.com/api/v1`
- **Official documentation:** [Add Data](https://github.com/ShowcaseSoftwareLtd/showcase-workshop-apis/blob/main/rest-api/README.md#add-data)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_name` | body | `string` | yes | Name for the submitted data payload. |
| `showcase_id` | body | `number` | yes | Numeric Showcase identifier that the data belongs to. |
| `user_email` | body | `string` | yes | Email address associated with the data submission. |
| `content` | body | `string` | yes | Submitted content as a JSON string. |
| `date_entered` | body | `date` | yes | ISO 8601 timestamp when the data was entered. |
