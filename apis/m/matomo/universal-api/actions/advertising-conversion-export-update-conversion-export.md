# Matomo: AdvertisingConversionExport update Conversion Export



```
PUT https://connect.mindcloud.co/v1/universal/matomo/latest/actions/advertising-conversion-export-update-conversion-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/advertising-conversion-export-update-conversion-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idExport": "string",
  "idSite": "1",
  "name": "Ava Chen",
  "type": "string",
  "parameters": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/matomo/latest/actions/advertising-conversion-export-update-conversion-export', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idExport": "string",
    "idSite": "1",
    "name": "Ava Chen",
    "type": "string",
    "parameters": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idExport` | string | yes | Matomo API parameter. |
| `idSite` | number | yes | Matomo API parameter. Default: `1`. |
| `name` | string | yes | Matomo API parameter. |
| `type` | string | yes | Matomo API parameter. |
| `parameters` | string | yes | Matomo API parameter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Matomo API parameter. |

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

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/advertising-conversion-export-update-conversion-export.md) for the provider-specific parameters and requirements.

