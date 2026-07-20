# Matomo: CustomAlerts edit Alert



```
GET https://connect.mindcloud.co/v1/universal/matomo/latest/actions/custom-alerts-edit-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/custom-alerts-edit-alert?connectionId=$CONNECTION_ID&idAlert=string&name=Ava%20Chen&idSites=1&period=day&emailMe=ava%40example.com&additionalEmails=ava%40example.com&phoneNumbers=string&metric=string&metricCondition=string&metricValue=string&comparedTo=string&reportUniqueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idAlert": "string",
  "name": "Ava Chen",
  "idSites": "1",
  "period": "day",
  "emailMe": "ava@example.com",
  "additionalEmails": "ava@example.com",
  "phoneNumbers": "string",
  "metric": "string",
  "metricCondition": "string",
  "metricValue": "string",
  "comparedTo": "string",
  "reportUniqueId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matomo/latest/actions/custom-alerts-edit-alert?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idAlert` | string | yes | Matomo API parameter. |
| `name` | string | yes | Matomo API parameter. |
| `idSites` | string | yes | Matomo API parameter. Default: `1`. |
| `period` | string | yes | Matomo API parameter. Default: `day`. |
| `emailMe` | string | yes | Matomo API parameter. |
| `additionalEmails` | string | yes | Matomo API parameter. |
| `phoneNumbers` | string | yes | Matomo API parameter. |
| `metric` | string | yes | Matomo API parameter. |
| `metricCondition` | string | yes | Matomo API parameter. |
| `metricValue` | string | yes | Matomo API parameter. |
| `comparedTo` | string | yes | Matomo API parameter. |
| `reportUniqueId` | string | yes | Matomo API parameter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reportCondition` | string | no | Matomo API parameter. |
| `reportValue` | string | no | Matomo API parameter. |
| `reportMediums` | string | no | Matomo API parameter. Default: `Array`. |
| `slackChannelID` | string | no | Matomo API parameter. |
| `msTeamsWebhookUrl` | string | no | Matomo API parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "label": "string",
      "nb_actions": 1,
      "nb_uniq_visitors": 1,
      "nb_visits": 1,
      "result": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `label` | string | Matomo response label |
| `nb_actions` | number | Actions |
| `nb_uniq_visitors` | number | Unique visitors |
| `nb_visits` | number | Visits |
| `result` | string | Operation result |
| `value` | string | Matomo response value |

## Native endpoint

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/custom-alerts-edit-alert.md) for the provider-specific parameters and requirements.

