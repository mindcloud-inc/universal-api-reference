# Gamalogic: Get Batch Status



```
GET https://connect.mindcloud.co/v1/universal/gamalogic/latest/actions/get-batch-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gamalogic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gamalogic/latest/actions/get-batch-status?connectionId=$CONNECTION_ID&batchId=100001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "batchId": "100001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gamalogic/latest/actions/get-batch-status?${params}`, {
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
| `batchId` | number | yes | Unique batch ID returned by the batch verification request. Example: `100001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": true,
      "processed": 1,
      "status": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | boolean | Whether the request returned an error. |
| `processed` | number | Number of email addresses processed. |
| `status` | string | Batch status such as processing or completed. |
| `total` | number | Total email addresses in the batch. |

## Native endpoint

Through the native Gamalogic API, this operation is `GET /batchstatus` (base URL `https://gamalogic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-status.md) for the provider-specific parameters and requirements.

