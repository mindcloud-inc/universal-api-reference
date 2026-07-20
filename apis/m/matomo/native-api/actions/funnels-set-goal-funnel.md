# Funnels set Goal Funnel with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [Funnels set Goal Funnel](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `idGoal` | body | `number` | yes | Matomo API parameter. |
| `isActivated` | body | `boolean` | yes | Matomo API parameter. |
| `steps` | body | `string` | no | Matomo API parameter. |
