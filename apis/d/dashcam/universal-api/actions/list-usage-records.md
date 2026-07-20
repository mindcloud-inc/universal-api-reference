# Dashcam: List Usage Records

Retrieves usage records from Dashcam.

```
GET https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/list-usage-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dashcam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/list-usage-records?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/list-usage-records?${params}`, {
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
| `page` | string | no |  |
| `perPage` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "page": 1,
      "perPage": 1,
      "records": [
        {}
      ],
      "total": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page` | number |  |
| `perPage` | number |  |
| `records` | array<object> |  |
| `total` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Dashcam API, this operation is `GET /api/billing/usage-records` (base URL `https://api.testdriver.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-usage-records.md) for the provider-specific parameters and requirements.

