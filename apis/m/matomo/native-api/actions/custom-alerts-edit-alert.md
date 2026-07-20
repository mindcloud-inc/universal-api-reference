# CustomAlerts edit Alert with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [CustomAlerts edit Alert](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idAlert` | body | `string` | yes | Matomo API parameter. |
| `name` | body | `string` | yes | Matomo API parameter. |
| `idSites` | body | `string` | yes | Matomo API parameter. |
| `period` | body | `string` | yes | Matomo API parameter. |
| `emailMe` | body | `string` | yes | Matomo API parameter. |
| `additionalEmails` | body | `string` | yes | Matomo API parameter. |
| `phoneNumbers` | body | `string` | yes | Matomo API parameter. |
| `metric` | body | `string` | yes | Matomo API parameter. |
| `metricCondition` | body | `string` | yes | Matomo API parameter. |
| `metricValue` | body | `string` | yes | Matomo API parameter. |
| `comparedTo` | body | `string` | yes | Matomo API parameter. |
| `reportUniqueId` | body | `string` | yes | Matomo API parameter. |
| `reportCondition` | body | `string` | no | Matomo API parameter. |
| `reportValue` | body | `string` | no | Matomo API parameter. |
| `reportMediums` | body | `string` | no | Matomo API parameter. |
| `slackChannelID` | body | `string` | no | Matomo API parameter. |
| `msTeamsWebhookUrl` | body | `string` | no | Matomo API parameter. |
