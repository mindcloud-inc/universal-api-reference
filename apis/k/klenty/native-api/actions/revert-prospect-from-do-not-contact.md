# Revert Prospect From Do Not Contact with Klenty

Reverts a prospect from do not contact in Klenty.

## Endpoint

- **Method:** `POST`
- **Path:** `/prospects/:email/revertStatusToDoNotContact`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Revert Prospect From Do Not Contact](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_849206f8a2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | Prospect email to revert from Do Not Contact. |
| `Email` | body | `string` | yes | Same prospect email, sent in the request body as required by Klenty. |
