# Get DQL Coverage Report By Query with Diffbot

Retrieves a DQL coverage report from Diffbot by query.

## Endpoint

- **Method:** `GET`
- **Path:** `https://kg.diffbot.com/kg/v3/dql/report`
- **Base URL:** `https://api.diffbot.com`
- **Official documentation:** [Get DQL Coverage Report By Query](https://docs.diffbot.com/reference/reportfind)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | DQL query string used to generate the coverage report. |
