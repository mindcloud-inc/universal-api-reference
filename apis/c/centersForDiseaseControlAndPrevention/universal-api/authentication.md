# Centers for Disease Control and Prevention Universal API Authentication

Every Centers for Disease Control and Prevention API request through MindCloud uses a MindCloud API key and the `connectionId` of a Centers for Disease Control and Prevention connection.

## How it works

1. [Create a MindCloud account](https://app.mindcloud.co/signup).
2. [Create a MindCloud API key](https://app.mindcloud.co/user/api-keys). Use it as the Bearer token on every request.
3. Open [Connections](https://app.mindcloud.co/credentials) and create your Centers for Disease Control and Prevention connection.
4. Close the connection modal, open the connection’s `•••` menu, and select **Copy Connection ID**.
5. Call any [Centers for Disease Control and Prevention action](README.md#actions-17) with your API key and `connectionId`.

Send the API key as `Authorization: Bearer $MINDCLOUD_API_KEY`. Pass `connectionId` in the query string for GET and DELETE requests, and in the JSON body for POST, PUT, and PATCH requests.
