# Rebrandly: Update Query Parameter

Updates a query parameter for a template in Rebrandly.

```
PUT https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/update-query-parameter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrandly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/update-query-parameter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "93a7720c6c684c2d91e3522d5672d7b5",
  "paramId": "ff4cd13109d34a4b92a4f28d0e4f8cff",
  "key": "mcstage3paramupdated",
  "format": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/update-query-parameter', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "93a7720c6c684c2d91e3522d5672d7b5",
    "paramId": "ff4cd13109d34a4b92a4f28d0e4f8cff",
    "key": "mcstage3paramupdated",
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
| `paramId` | string | yes | Query parameter identifier returned by List Query Parameters or Create Query Parameter. Example: `ff4cd13109d34a4b92a4f28d0e4f8cff`. |
| `label` | string | no | Updated human-friendly label for the query parameter. Example: `MindCloud Stage 3 Param Updated`. |
| `key` | string | yes | Updated query parameter key. Example: `mcstage3paramupdated`. |
| `format` | string | yes | Updated query parameter type. Example: `string`. |
| `options[]` | array<object> | no | Updated preset options when format is preset. |
| `placeholder` | string | no | Updated dashboard placeholder. Example: `Insert an updated value`. |
| `default` | string | no | Updated default value. Example: `updated-default`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rebrandly API returns.

## Native endpoint

Through the native Rebrandly API, this operation is `POST https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/params/:paramId` (base URL `https://api.rebrandly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-query-parameter.md) for the provider-specific parameters and requirements.

