# AbTesting add Experiment with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [AbTesting add Experiment](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `name` | body | `string` | yes | Matomo API parameter. |
| `hypothesis` | body | `string` | yes | Matomo API parameter. |
| `description` | body | `string` | yes | Matomo API parameter. |
| `variations` | body | `string` | yes | Matomo API parameter. |
| `includedTargets` | body | `string` | yes | Matomo API parameter. |
| `successMetrics` | body | `string` | yes | Matomo API parameter. |
