# Xodo Sign: List Bulk Jobs

Retrieves bulk jobs from Xodo Sign.

```
GET https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/list-bulk-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xodo Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/list-bulk-jobs?connectionId=$CONNECTION_ID&business_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "business_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/list-bulk-jobs?${params}`, {
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
| `business_id` | string | yes | The Xodo Sign business ID that owns the bulk jobs. |
| `limit` | number | no | Maximum amount of jobs to fetch. |
| `offset` | number | no | Number of jobs to skip when fetching results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Bulk jobs returned for the current user and business. |
| `pagination` | object | Pagination metadata for the bulk jobs result set. |

## Native endpoint

Through the native Xodo Sign API, this operation is `GET /bulk_job` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bulk-jobs.md) for the provider-specific parameters and requirements.

