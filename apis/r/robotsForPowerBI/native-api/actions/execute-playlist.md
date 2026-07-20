# Execute playlist with Robots for Power BI

Executes a playlist in Robots for Power BI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/playlist.execute`
- **Base URL:** `https://www.powerbitiles.com/PBIRobots`
- **Official documentation:** [Execute playlist](https://www.powerbitiles.com/PBIRobots/docs/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | PowerBI Robots playlist UUID to execute. |
