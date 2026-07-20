# Funnels save Non Goal Funnel with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [Funnels save Non Goal Funnel](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `idFunnel` | body | `string` | yes | Matomo API parameter. |
| `funnelName` | body | `string` | yes | Matomo API parameter. |
| `steps` | body | `string` | yes | Matomo API parameter. |
