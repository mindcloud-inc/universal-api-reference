# OAuth2 set Client Active with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [OAuth2 set Client Active](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientId` | body | `string` | yes | Matomo API parameter. |
| `active` | body | `string` | yes | Matomo API parameter. |
