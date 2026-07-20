# Get Client with Climbo 2.0

Retrieves a client from Climbo 2.0.

## Endpoint

- **Method:** `GET`
- **Path:** `/client/{client_id}`
- **Base URL:** `https://api.climbo.com`
- **Official documentation:** [Get Client](https://climbo.readme.io/reference/get-client)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | path | `string` | yes | ID of your customer. |
| `login_link` | query | `boolean` | no | Whether to return a login link. |
