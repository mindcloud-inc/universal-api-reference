# Makeplans: List Service Slots

Retrieves available service slots from Makeplans.

```
GET https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/list-service-slots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeplans `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/list-service-slots?connectionId=$CONNECTION_ID&serviceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "serviceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/list-service-slots?${params}`, {
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
| `serviceId` | number | yes | The Makeplans service ID. |
| `from` | date | no | Start date for slot lookup. Defaults to today. |
| `to` | date | no | End date for slot lookup. Defaults to today. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "available_resources": [
        1
      ],
      "formatted_timestamp": "string",
      "formatted_timestamp_end": "string",
      "free": 1,
      "maximum_capacity": 1,
      "timestamp": "2026-05-07T12:00:00.000Z",
      "timestamp_end": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available_resources` | array<number> |  |
| `formatted_timestamp` | string |  |
| `formatted_timestamp_end` | string |  |
| `free` | number |  |
| `maximum_capacity` | number |  |
| `timestamp` | date |  |
| `timestamp_end` | date |  |

## Native endpoint

Through the native Makeplans API, this operation is `GET /services/:serviceId/slots` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-service-slots.md) for the provider-specific parameters and requirements.

