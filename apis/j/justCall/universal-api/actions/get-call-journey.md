# JustCall: Get Call Journey

Retrieves a call journey from JustCall.

```
GET https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-call-journey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustCall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-call-journey?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-call-journey?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callSid": "string",
      "id": 1,
      "journeys": [
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
| `callSid` | string |  |
| `id` | number |  |
| `journeys` | array<object> |  |

## Native endpoint

Through the native JustCall API, this operation is `GET /v2.1/calls/:id/journey` (base URL `https://api.justcall.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-journey.md) for the provider-specific parameters and requirements.

