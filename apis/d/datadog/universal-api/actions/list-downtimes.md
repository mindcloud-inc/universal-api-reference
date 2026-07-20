# Datadog: List Downtimes

Retrieves downtimes from Datadog.

```
GET https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-downtimes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-downtimes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-downtimes?${params}`, {
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
| `currentOnly` | boolean | no | Return only currently active downtimes. |
| `include` | string | no | Additional related resources to include. |
| `pageLimit` | number | no | Maximum number of downtimes to return. |
| `pageOffset` | number | no | Pagination offset for downtimes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Downtime records returned by the list request. |
| `meta` | object | Pagination metadata for the downtime list. |

## Native endpoint

Through the native Datadog API, this operation is `GET /api/v2/downtime` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-downtimes.md) for the provider-specific parameters and requirements.

