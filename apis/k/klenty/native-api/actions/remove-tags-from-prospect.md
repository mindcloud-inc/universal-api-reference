# Remove Tags From Prospect with Klenty

Removes tags from a prospect in Klenty.

## Endpoint

- **Method:** `POST`
- **Path:** `/prospects/:email/removeTags`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Remove Tags From Prospect](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_4a906927ed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | Prospect email to remove tags from. |
| `tag` | body | `list<string>` | yes | One or more tags to remove from the prospect. Send an array of tag strings. |
