# List Webhooks with SonarQube

Retrieves webhooks from SonarQube.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/webhooks/list`
- **Base URL:** `https://sonarcloud.io`
- **Official documentation:** [List Webhooks](https://sonarcloud.io/web_api/api/webhooks/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | query | `string` | yes | Organization key. Required by /api/webhooks/list. |
