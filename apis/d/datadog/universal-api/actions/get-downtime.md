# Datadog: Get Downtime

Retrieves a downtime from Datadog.

```
GET https://connect.mindcloud.co/v1/universal/datadog/latest/actions/get-downtime
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/get-downtime?connectionId=$CONNECTION_ID&downtimeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "downtimeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datadog/latest/actions/get-downtime?${params}`, {
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
| `downtimeId` | string | yes | The ID of the downtime. |
| `include` | string | no | Additional related resources to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "included": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Downtime record returned by the request. |
| `included` | array<object> | Related resources included by the response. |

## Native endpoint

Through the native Datadog API, this operation is `GET /api/v2/downtime/:downtime_id` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-downtime.md) for the provider-specific parameters and requirements.

