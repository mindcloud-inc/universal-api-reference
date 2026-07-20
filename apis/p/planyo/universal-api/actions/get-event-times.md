# Planyo: Get Event Times

Retrieves event times from Planyo.

```
GET https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-event-times
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planyo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-event-times?connectionId=$CONNECTION_ID&resourceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-event-times?${params}`, {
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
| `resourceId` | number | yes |  |
| `format` | string | no |  |
| `futureOnly` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": "string",
      "eventTimes": [
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
| `duration` | string |  |
| `eventTimes` | array<object> |  |

## Native endpoint

Through the native Planyo API, this operation is `GET /` (base URL `https://www.planyo.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-times.md) for the provider-specific parameters and requirements.

