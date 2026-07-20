# Perform a URL analysis with Routee

Analyzes a URL request in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/urlinsights`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Perform a URL analysis](https://docs.routee.net/reference/perform-a-url-analysis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cache` | body | `boolean` | no | Get a cached response from our databases or get a synchronous response. |
| `domain` | body | `string` | yes | The domain for which we need an analysis. |
