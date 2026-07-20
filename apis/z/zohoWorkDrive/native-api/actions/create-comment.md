# Create Comment with Zoho WorkDrive

Creates a new comment in Zoho WorkDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/comments`
- **Base URL:** `{api_domain}/workdrive`
- **Official documentation:** [Create Comment](https://workdrive.zoho.com/apidocs/v1/comments/createcomment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.resource_id` | body | `string` | yes | The file or folder resource ID to comment on. |
| `data.attributes.comment_html` | body | `string` | yes | The comment body as HTML. |
