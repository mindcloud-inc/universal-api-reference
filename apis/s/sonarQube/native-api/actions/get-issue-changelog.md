# Get Issue Changelog with SonarQube

Retrieves an issue changelog from SonarQube.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/issues/changelog`
- **Base URL:** `https://sonarcloud.io`
- **Official documentation:** [Get Issue Changelog](https://sonarcloud.io/web_api/api/issues/changelog)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issue` | query | `string` | yes | Issue key whose changelog should be returned. Required by /api/issues/changelog. |
