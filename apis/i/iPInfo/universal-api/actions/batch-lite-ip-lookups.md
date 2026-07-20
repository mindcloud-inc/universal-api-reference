# IPInfo: Batch Lite IP Lookups



```
GET https://connect.mindcloud.co/v1/universal/iPInfo/latest/actions/batch-lite-ip-lookups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IPInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPInfo/latest/actions/batch-lite-ip-lookups?connectionId=$CONNECTION_ID&requests=8.8.8.8%2C1.1.1.1%2Fcountry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requests": "8.8.8.8,1.1.1.1/country"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPInfo/latest/actions/batch-lite-ip-lookups?${params}`, {
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
| `requests` | string | yes | JSON array of IPs or URL patterns to enrich in the Lite batch endpoint. Example: `8.8.8.8,1.1.1.1/country`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native IPInfo API returns.

## Native endpoint

Through the native IPInfo API, this operation is `POST /batch/lite` (base URL `https://api.ipinfo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-lite-ip-lookups.md) for the provider-specific parameters and requirements.

