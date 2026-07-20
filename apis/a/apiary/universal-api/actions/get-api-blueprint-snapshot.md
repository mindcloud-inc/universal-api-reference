# Apiary: Get API Blueprint Snapshot



```
GET https://connect.mindcloud.co/v1/universal/apiary/latest/actions/get-api-blueprint-snapshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apiary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apiary/latest/actions/get-api-blueprint-snapshot?connectionId=$CONNECTION_ID&apiName=mindcloudapp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "apiName": "mindcloudapp"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apiary/latest/actions/get-api-blueprint-snapshot?${params}`, {
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
| `apiName` | string | yes | Select the Apiary API subdomain to fetch the blueprint snapshot for. Example: `mindcloudapp`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Apiary API returns.

## Native endpoint

Through the native Apiary API, this operation is `GET https://jsapi.apiary.io/apis/{{apiName}}/blueprint` (base URL `https://api.apiary.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-blueprint-snapshot.md) for the provider-specific parameters and requirements.

