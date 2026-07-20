# Invidious: Get Mix



```
GET https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-mix
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-mix?connectionId=$CONNECTION_ID&mixId=RDCLAK5uy..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mixId": "RDCLAK5uy..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-mix?${params}`, {
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
| `mixId` | string | yes | Mix/radio playlist ID. Example: `RDCLAK5uy...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mixId": "string",
      "title": "string",
      "videos": [
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
| `mixId` | string |  |
| `title` | string |  |
| `videos` | array<object> |  |

## Native endpoint

Through the native Invidious API, this operation is `GET /mixes/:rdid` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mix.md) for the provider-specific parameters and requirements.

