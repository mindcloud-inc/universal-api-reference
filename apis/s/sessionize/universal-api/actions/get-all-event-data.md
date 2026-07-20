# Sessionize: Get All Event Data

Retrieves all event data from Sessionize.

```
GET https://connect.mindcloud.co/v1/universal/sessionize/latest/actions/get-all-event-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sessionize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sessionize/latest/actions/get-all-event-data?connectionId=$CONNECTION_ID&endpointId=jl4ktls0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endpointId": "jl4ktls0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sessionize/latest/actions/get-all-event-data?${params}`, {
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
| `endpointId` | string | yes | Sessionize event API endpoint ID from URLs like https://sessionize.com/api/v2/{endpointId}/view/All. Default: `jl4ktls0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        {}
      ],
      "questions": [
        {}
      ],
      "rooms": [
        {}
      ],
      "sessions": [
        {}
      ],
      "speakers": [
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
| `categories` | array<object> | Session and speaker categories. |
| `questions` | array<object> | Custom questions configured for the endpoint. |
| `rooms` | array<object> | Event rooms. |
| `sessions` | array<object> | Event sessions returned by the endpoint. |
| `speakers` | array<object> | Event speakers returned by the endpoint. |

## Native endpoint

Through the native Sessionize API, this operation is `GET /api/v2/:endpointId/view/All` (base URL `https://sessionize.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-event-data.md) for the provider-specific parameters and requirements.

