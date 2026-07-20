# SIGNL4: Get Event Parameters

Retrieves event parameters from SIGNL4.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-event-parameters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-event-parameters?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-event-parameters?${params}`, {
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
| `eventId` | string | yes | Event Id of the requested Alert. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "order": 1,
      "type": 1,
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `order` | number |  |
| `type` | number |  |
| `value` | string |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `GET /v2/events/{eventId}/parameters` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-parameters.md) for the provider-specific parameters and requirements.

