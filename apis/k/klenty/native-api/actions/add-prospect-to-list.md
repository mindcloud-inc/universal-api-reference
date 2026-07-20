# Add Prospect To List with Klenty

Adds a prospect to a list in Klenty.

## Endpoint

- **Method:** `POST`
- **Path:** `/prospects`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Add Prospect To List](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_8848b48485)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Email` | body | `string` | yes | Prospect email address. |
| `FirstName` | body | `string` | no | Prospect first name. |
| `List` | body | `string` | yes | List name to add the prospect to. |
