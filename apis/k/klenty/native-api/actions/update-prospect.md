# Update Prospect with Klenty

Updates an existing prospect in Klenty.

## Endpoint

- **Method:** `POST`
- **Path:** `/prospects/:email`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Update Prospect](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_3315dd4ccc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | Prospect email to update. |
| `FirstName` | body | `string` | yes | Updated first name for the prospect. |
