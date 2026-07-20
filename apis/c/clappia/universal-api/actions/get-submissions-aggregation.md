# Clappia: Get Submissions Aggregation

Retrieves submission aggregation results from Clappia.

```
GET https://connect.mindcloud.co/v1/universal/clappia/latest/actions/get-submissions-aggregation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clappia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/get-submissions-aggregation?connectionId=$CONNECTION_ID&appId=string&requestingUserEmailAddress=ava%40example.com&aggregationDimensions%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string",
  "requestingUserEmailAddress": "ava@example.com",
  "aggregationDimensions[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clappia/latest/actions/get-submissions-aggregation?${params}`, {
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
| `appId` | string | yes | Clappia app ID. |
| `requestingUserEmailAddress` | string | yes | Email address of the Clappia user on whose behalf aggregation should run. |
| `aggregationDimensions[]` | array<object> | yes | Array of aggregation dimension objects describing the metrics to calculate. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dimensions[]` | array<object> | no | Optional array of dimension objects for grouping aggregation results. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clappia API returns.

## Native endpoint

Through the native Clappia API, this operation is `POST /submissions/getSubmissionsAggregation` (base URL `https://api-public-v4.clappia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-submissions-aggregation.md) for the provider-specific parameters and requirements.

