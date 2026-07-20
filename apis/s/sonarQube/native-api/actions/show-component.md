# Show Component with SonarQube

Retrieves a component from SonarQube.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/components/show`
- **Base URL:** `https://sonarcloud.io`
- **Official documentation:** [Show Component](https://sonarcloud.io/web_api/api/components/show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `component` | query | `string` | yes | Component key to show. Required by /api/components/show. |
