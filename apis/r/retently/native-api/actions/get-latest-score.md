# Get Latest Score with Retently

Retrieves the latest metric score from Retently.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/:metric/score`
- **Base URL:** `https://app.retently.com`
- **Official documentation:** [Get Latest Score](https://www.retently.com/api/#api-get-latest-score-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metric` | path | `string` | yes | Metric key such as nps, csat, or ces. |
