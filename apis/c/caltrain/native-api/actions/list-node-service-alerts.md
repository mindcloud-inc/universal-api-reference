# List Node Service Alerts with Caltrain

Retrieves service alerts for a Caltrain node.

## Endpoint

- **Method:** `GET`
- **Path:** `/gtfs/api/v1/servicealerts/:nodeId`
- **Base URL:** `https://www.caltrain.com`
- **Official documentation:** [List Node Service Alerts](https://www.caltrain.com/developer-resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nodeId` | path | `string` | yes | Caltrain route or stop node identifier such as 7840. |
