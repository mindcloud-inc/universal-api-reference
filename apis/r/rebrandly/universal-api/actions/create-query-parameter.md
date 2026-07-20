# Rebrandly: Create Query Parameter

Creates a query parameter for a template in Rebrandly.

```
POST https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/create-query-parameter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrandly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/create-query-parameter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "93a7720c6c684c2d91e3522d5672d7b5",
  "key": "mcstage3param",
  "label": "MindCloud Stage 3 Param",
  "format": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/create-query-parameter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "93a7720c6c684c2d91e3522d5672d7b5",
    "key": "mcstage3param",
    "label": "MindCloud Stage 3 Param",
    "format": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Template identifier returned by List Templates. Example: `93a7720c6c684c2d91e3522d5672d7b5`. |
| `key` | string | yes | Key of the query string pair. Example: `mcstage3param`. |
| `label` | string | yes | Human-friendly label for the query parameter. Example: `MindCloud Stage 3 Param`. |
| `format` | string | yes | Query parameter type: string or preset. Example: `string`. |
| `options[]` | array<object> | no | Preset option values when format is preset. |
| `placeholder` | string | no | Placeholder shown in the dashboard UTM builder. Example: `Insert a value for this custom param`. |
| `default` | string | no | Default value for the query parameter. Example: `stage3-default`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rebrandly API returns.

## Native endpoint

Through the native Rebrandly API, this operation is `POST https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/params` (base URL `https://api.rebrandly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-query-parameter.md) for the provider-specific parameters and requirements.

