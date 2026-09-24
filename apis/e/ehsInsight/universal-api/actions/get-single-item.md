# EHS Insight: Get Single Item



```
GET https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/get-single-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EHS Insight `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/get-single-item?connectionId=$CONNECTION_ID&rowuid=26686a13-5b64-4b0d-9376-91f36cb728ff&entityName=UserContact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rowuid": "26686a13-5b64-4b0d-9376-91f36cb728ff",
  "entityName": "UserContact"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/get-single-item?${params}`, {
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
| `rowuid` | string | yes | Default: `26686a13-5b64-4b0d-9376-91f36cb728ff`. |
| `entityName` | string | yes | Default: `UserContact`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EHS Insight API returns.

## Native endpoint

Through the native EHS Insight API, this operation is `GET /v4/entity/:entityName/fetch/:rowuid` (base URL `https://{{credentials.companyName}}.ehsinsight.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-single-item.md) for the provider-specific parameters and requirements.

