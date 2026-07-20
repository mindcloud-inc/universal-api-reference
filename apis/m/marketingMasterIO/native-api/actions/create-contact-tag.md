# Create Contact Tag with Marketing Master IO

Creates a new contact tag in Marketing Master IO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contacts/tags`
- **Base URL:** `https://api.marketingmaster.io`
- **Official documentation:** [Create Contact Tag](https://developers.marketingmaster.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Contact tag name. |
| `page_data_id` | body | `string` | yes | Page data ID associated with the tag. |
