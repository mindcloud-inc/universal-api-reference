# Get Authenticated User with Stackoverflow

Retrieves the authenticated user from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/me`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [Get Authenticated User](https://api.stackexchange.com/docs/me)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site` | query | `string` | yes | The Stack Exchange site context to use when resolving the authenticated user, such as stackoverflow. |
