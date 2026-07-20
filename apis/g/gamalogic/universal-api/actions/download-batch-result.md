# Gamalogic: Download Batch Result



```
GET https://connect.mindcloud.co/v1/universal/gamalogic/latest/actions/download-batch-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gamalogic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gamalogic/latest/actions/download-batch-result?connectionId=$CONNECTION_ID&batchId=100001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "batchId": "100001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gamalogic/latest/actions/download-batch-result?${params}`, {
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
| `batchId` | number | yes | Unique batch ID for the completed batch verification request. Example: `100001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": true,
      "gamalogicEmailidVrfy": [
        {}
      ],
      "resolvedTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | boolean | Whether the request returned an error. |
| `gamalogicEmailidVrfy` | array<object> | Resolved email verification result rows. |
| `resolvedTime` | string | Total time taken to resolve the list. |

## Native endpoint

Through the native Gamalogic API, this operation is `GET /batchresult` (base URL `https://gamalogic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-batch-result.md) for the provider-specific parameters and requirements.

