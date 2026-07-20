# Get Weather Metrics with wttr.in

Retrieves Prometheus weather metrics from wttr.in.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:location]`
- **Base URL:** `https://wttr.in`
- **Official documentation:** [Get Weather Metrics](https://github.com/chubin/wttr.in#prometheus-metrics-output)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | path | `string` | yes | City, airport code, domain, postal code, GPS coordinates, or supported wttr.in location expression. |
