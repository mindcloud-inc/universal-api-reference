# Lulu: Get Print Job

Retrieves a print job from Lulu.

```
GET https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-print-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lulu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-print-job?connectionId=$CONNECTION_ID&id=job_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "job_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-print-job?${params}`, {
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
| `id` | string | yes | Lulu print job ID. Default: `job_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "childJobIds": [
        [
          1
        ]
      ],
      "items": [
        [
          {}
        ]
      ],
      "lineItems": [
        [
          {}
        ]
      ],
      "parentJobId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `childJobIds[]` | array<number> |  |
| `items[]` | array<object> |  |
| `items[].reprint` | object |  |
| `items[].reprint.defect` | string |  |
| `lineItems[]` | array<object> |  |
| `lineItems[].reprint` | object |  |
| `lineItems[].reprint.defect` | string |  |
| `parentJobId` | number |  |

## Native endpoint

Through the native Lulu API, this operation is `GET /print-jobs/{id}/` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-print-job.md) for the provider-specific parameters and requirements.

