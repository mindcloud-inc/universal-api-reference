# Change Prospect To Do Not Contact with Klenty

Changes a prospect to do not contact in Klenty.

## Endpoint

- **Method:** `POST`
- **Path:** `/prospects/:email/changeStatusToDoNotContact`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Change Prospect To Do Not Contact](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_99a462c518)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | Prospect email to change to Do Not Contact. |
| `Email` | body | `string` | yes | Same prospect email, sent in the request body as required by Klenty. |
