# Matomo: PrivacyManager anonymize Some Raw Data



```
GET https://connect.mindcloud.co/v1/universal/matomo/latest/actions/privacy-manager-anonymize-some-raw-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/privacy-manager-anonymize-some-raw-data?connectionId=$CONNECTION_ID&idSites=1&date=yesterday" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idSites": "1",
  "date": "yesterday"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matomo/latest/actions/privacy-manager-anonymize-some-raw-data?${params}`, {
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
| `idSites` | string | yes | Matomo API parameter. Default: `1`. |
| `date` | string | yes | Matomo API parameter. Default: `yesterday`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `anonymizeIp` | string | no | Matomo API parameter. |
| `anonymizeLocation` | string | no | Matomo API parameter. |
| `anonymizeUserId` | string | no | Matomo API parameter. |
| `unsetVisitColumns` | string | no | Matomo API parameter. Default: `Array`. |
| `unsetLinkVisitActionColumns` | string | no | Matomo API parameter. Default: `Array`. |
| `passwordConfirmation` | string | no | Matomo API parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "label": "string",
      "nb_actions": 1,
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
| `nb_visits` | number | Visits |
| `result` | string | Operation result |
| `value` | string | Matomo response value |

## Native endpoint

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/privacy-manager-anonymize-some-raw-data.md) for the provider-specific parameters and requirements.

