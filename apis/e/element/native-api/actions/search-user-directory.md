# Search User Directory with Element

Finds users in Element by search term.

## Endpoint

- **Method:** `POST`
- **Path:** `/_matrix/client/v3/user_directory/search`
- **Base URL:** `{homeserverUrl}`
- **Official documentation:** [Search User Directory](https://spec.matrix.org/latest/client-server-api/#post_matrixclientv3user_directorysearch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_term` | body | `string` | yes | Case-insensitive term to match against the user directory. |
