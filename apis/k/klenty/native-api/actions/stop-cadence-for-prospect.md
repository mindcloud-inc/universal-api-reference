# Stop Cadence For Prospect with Klenty

Stops cadence for a prospect in Klenty.

## Endpoint

- **Method:** `POST`
- **Path:** `/stopcadence`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Stop Cadence For Prospect](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_a2e9edeb59)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cadenceName` | body | `string` | no | Cadence name to stop for the prospect. Leave empty to remove from all cadences. |
| `Email` | body | `string` | yes | Prospect email to remove from a cadence. |
