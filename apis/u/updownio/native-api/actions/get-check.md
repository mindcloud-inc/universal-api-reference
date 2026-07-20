# Get Check with updown.io

Retrieves a monitoring check from updown.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/checks/:token`
- **Base URL:** `https://updown.io/api`
- **Official documentation:** [Get Check](https://updown.io/api#GET-/api/checks/:token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metrics` | query | `boolean` | no | Include performance metrics from the last hour. |
| `token` | path | `string` | yes | The check unique token. |
