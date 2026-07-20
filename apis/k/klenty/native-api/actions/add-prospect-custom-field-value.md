# Add Prospect Custom Field Value with Klenty

Adds a custom field value to a prospect in Klenty.

## Endpoint

- **Method:** `POST`
- **Path:** `/prospects`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Add Prospect Custom Field Value](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_fa068477d0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Email` | body | `string` | yes | Prospect email address. |
| `FirstName` | body | `string` | no | Prospect first name. |
| `CustomFields` | body | `list<object>` | yes | List of custom field key/value objects to set on the prospect. |
