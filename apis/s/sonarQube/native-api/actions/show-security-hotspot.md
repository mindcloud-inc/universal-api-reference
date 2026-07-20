# Show Security Hotspot with SonarQube

Retrieves a security hotspot from SonarQube.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/hotspots/show`
- **Base URL:** `https://sonarcloud.io`
- **Official documentation:** [Show Security Hotspot](https://sonarcloud.io/web_api/api/hotspots/show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hotspot` | query | `string` | yes | Security hotspot key. Required by /api/hotspots/show. |
