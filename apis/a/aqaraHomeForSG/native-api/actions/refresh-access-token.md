# Refresh Access Token with Aqara Home for SG

Refreshes access and refresh tokens in Aqara Home for SG.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3.0/open/api`
- **Base URL:** `https://open-sg.aqara.com`
- **Official documentation:** [Refresh Access Token](https://opendoc.aqara.com/en/docs/developmanual/authManagement/aqaraauthMode.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.refreshToken` | body | `string` | yes | Aqara refresh token returned by Get Access Token. |
