# JustCall: Get a Thread

Retrieves a text thread from JustCall.

```
GET https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-a-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustCall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-a-thread?connectionId=$CONNECTION_ID&threadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "threadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-a-thread?${params}`, {
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
| `threadId` | string | yes |  |
| `offset` | number | no |  |
| `limit` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "nextPageLink": "https://example.com",
      "prevPageLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `nextPageLink` | string |  |
| `prevPageLink` | string |  |

## Native endpoint

Through the native JustCall API, this operation is `GET /v2.1/texts/threads/:thread_id` (base URL `https://api.justcall.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-thread.md) for the provider-specific parameters and requirements.

