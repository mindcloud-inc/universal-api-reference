# List User Cadences with Klenty

Retrieves user cadences from Klenty.

## Endpoint

- **Method:** `GET`
- **Path:** `/cadences`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [List User Cadences](https://support.klenty.com/en/articles/8193357-klenty-s-get-api-s#h_80a1c4f4b5)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | query | `string` | yes | Team member email address whose cadences should be listed. |
