# List Workplace Users with Clappia

Retrieves workplace users from your Clappia workplace.

## Endpoint

- **Method:** `POST`
- **Path:** `/workplace/getWorkplaceUsers`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [List Workplace Users](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageSize` | body | `number` | no | Maximum number of users to return. |
| `token` | body | `string` | no | Token returned by a previous workplace users response. |
