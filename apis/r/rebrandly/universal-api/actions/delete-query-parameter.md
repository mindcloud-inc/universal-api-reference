# Rebrandly: Delete Query Parameter

Deletes a query parameter from a template in Rebrandly.

```
DELETE https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/delete-query-parameter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrandly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/delete-query-parameter?connectionId=$CONNECTION_ID&templateId=93a7720c6c684c2d91e3522d5672d7b5&paramId=ff4cd13109d34a4b92a4f28d0e4f8cff" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "93a7720c6c684c2d91e3522d5672d7b5",
  "paramId": "ff4cd13109d34a4b92a4f28d0e4f8cff"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/delete-query-parameter?${params}`, {
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
| `templateId` | string | yes | Template identifier returned by List Templates. Example: `93a7720c6c684c2d91e3522d5672d7b5`. |
| `paramId` | string | yes | Query parameter identifier returned by List Query Parameters or Create Query Parameter. Example: `ff4cd13109d34a4b92a4f28d0e4f8cff`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rebrandly API returns.

## Native endpoint

Through the native Rebrandly API, this operation is `DELETE https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/params/:paramId` (base URL `https://api.rebrandly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-query-parameter.md) for the provider-specific parameters and requirements.

