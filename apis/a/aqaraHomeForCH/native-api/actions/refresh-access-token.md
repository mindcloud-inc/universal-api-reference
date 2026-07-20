# Refresh Access Token with Aqara Home for CH

Refreshes Aqara access and refresh tokens with a refresh token.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3.0/open/api`
- **Base URL:** `https://open-cn.aqara.com`
- **Official documentation:** [Refresh Access Token](https://opendoc.aqara.com/en/docs/developmanual/authManagement/aqaraauthMode.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Aqara request data object for the selected intent. |
