# Create Email List with Toofr

Creates a new email list in Toofr.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists`
- **Base URL:** `https://www.findemails.com/api/v1`
- **Official documentation:** [Create Email List](https://developer.findemails.com/?from=explinks.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | query | `string` | no | Optional email list description. |
| `file_type` | query | `string` | no | Optional list file type. |
| `name` | query | `string` | yes | Name for the email list. |
