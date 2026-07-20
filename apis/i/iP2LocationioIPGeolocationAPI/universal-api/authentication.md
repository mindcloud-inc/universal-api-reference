# IP2Location.io IP Geolocation Universal API Authentication

Every IP2Location.io IP Geolocation API request through MindCloud uses a MindCloud API key and the `connectionId` of a IP2Location.io IP Geolocation connection.

## How it works

1. [Create a MindCloud account](https://app.mindcloud.co/signup).
2. [Create a MindCloud API key](https://app.mindcloud.co/user/api-keys). Use it as the Bearer token on every request.
3. Open [Connections](https://app.mindcloud.co/credentials) and create your IP2Location.io IP Geolocation connection.
4. Close the connection modal, open the connection’s `•••` menu, and select **Copy Connection ID**.
5. Call any [IP2Location.io IP Geolocation action](README.md#actions-3) with your API key and `connectionId`.

Send the API key as `Authorization: Bearer $MINDCLOUD_API_KEY`. Pass `connectionId` in the query string for GET and DELETE requests, and in the JSON body for POST, PUT, and PATCH requests.
