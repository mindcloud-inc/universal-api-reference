# Unsubscribe Prospect with Klenty

Unsubscribes a prospect in Klenty.

## Endpoint

- **Method:** `POST`
- **Path:** `/prospects/:email/unsubscribe`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Unsubscribe Prospect](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_7860116467)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | Prospect email to unsubscribe. |
| `Email` | body | `string` | yes | Same prospect email, sent in the request body as required by Klenty. |
