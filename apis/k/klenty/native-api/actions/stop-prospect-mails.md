# Stop Prospect Mails with Klenty

Stops mails for a prospect in Klenty.

## Endpoint

- **Method:** `POST`
- **Path:** `/prospects/:email/stop`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Stop Prospect Mails](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_47985d38d5)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | Prospect email to stop scheduled mails for. |
| `Email` | body | `string` | yes | Same prospect email, sent in the request body as required by Klenty. |
