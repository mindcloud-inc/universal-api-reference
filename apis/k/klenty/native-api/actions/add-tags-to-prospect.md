# Add Tags To Prospect with Klenty

Adds tags to a prospect in Klenty.

## Endpoint

- **Method:** `POST`
- **Path:** `/prospects`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Add Tags To Prospect](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_8ab1e33aa8)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Email` | body | `string` | yes | Prospect email address. |
| `FirstName` | body | `string` | no | Prospect first name. |
| `Tags` | body | `string` | yes | Pipe-delimited tag names to assign. |
