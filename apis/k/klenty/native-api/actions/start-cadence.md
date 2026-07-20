# Start Cadence with Klenty

Starts a cadence in Klenty.

## Endpoint

- **Method:** `POST`
- **Path:** `/startcadence`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Start Cadence](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_c4b3f24c10)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Email` | body | `string` | yes | Prospect email address. |
| `cadenceName` | body | `string` | yes | Cadence name to start for the prospect. |
