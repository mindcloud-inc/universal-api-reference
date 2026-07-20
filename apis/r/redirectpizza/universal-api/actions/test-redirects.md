# redirect.pizza: Test Redirects



```
GET https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/test-redirects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a redirect.pizza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/test-redirects?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/test-redirects?${params}`, {
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
| `url` | string | yes | URL to test. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": 1,
      "error": "string",
      "explanation": "string",
      "headers": {},
      "nextTestUrl": "https://example.com",
      "redirect": {},
      "status": "string",
      "statusCode": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration` | number |  |
| `error` | string |  |
| `explanation` | string |  |
| `headers` | object |  |
| `nextTestUrl` | string |  |
| `redirect` | object |  |
| `status` | string |  |
| `statusCode` | number |  |
| `url` | string |  |

## Native endpoint

Through the native redirect.pizza API, this operation is `GET /api/v1/tester` (base URL `https://redirect.pizza`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-redirects.md) for the provider-specific parameters and requirements.

