# Get Authorization Code with Aqara Home for CH

Retrieves an Aqara authorization code for account access.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3.0/open/api`
- **Base URL:** `https://open-cn.aqara.com`
- **Official documentation:** [Get Authorization Code](https://opendoc.aqara.com/en/docs/developmanual/authManagement/aqaraauthMode.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Aqara request data object for the selected intent. |
