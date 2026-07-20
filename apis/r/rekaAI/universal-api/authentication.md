# Reka AI Universal API Authentication

Every Reka AI API request through MindCloud uses a MindCloud API key and the `connectionId` of a Reka AI connection.

## How it works

1. [Create a MindCloud account](https://app.mindcloud.co/signup).
2. [Create a MindCloud API key](https://app.mindcloud.co/user/api-keys). Use it as the Bearer token on every request.
3. Open [Connections](https://app.mindcloud.co/credentials) and create your Reka AI connection.
4. Close the connection modal, open the connection’s `•••` menu, and select **Copy Connection ID**.
5. Call any [Reka AI action](README.md#actions-50) with your API key and `connectionId`.

Send the API key as `Authorization: Bearer $MINDCLOUD_API_KEY`. Pass `connectionId` in the query string for GET and DELETE requests, and in the JSON body for POST, PUT, and PATCH requests.
