# OAuth2 update Client with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [OAuth2 update Client](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientId` | body | `string` | yes | Matomo API parameter. |
| `name` | body | `string` | yes | Matomo API parameter. |
| `grantTypes` | body | `string` | yes | Matomo API parameter. |
| `scope` | body | `string` | yes | Matomo API parameter. |
| `redirectUris` | body | `string` | no | Matomo API parameter. |
| `description` | body | `string` | no | Matomo API parameter. |
| `type` | body | `string` | no | Matomo API parameter. |
| `active` | body | `string` | no | Matomo API parameter. |
