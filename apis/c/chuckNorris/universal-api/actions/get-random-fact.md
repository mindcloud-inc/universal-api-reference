# Chuck Norris: Get Random Fact



```
GET https://connect.mindcloud.co/v1/universal/chuckNorris/latest/actions/get-random-fact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chuck Norris `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chuckNorris/latest/actions/get-random-fact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chuckNorris/latest/actions/get-random-fact?${params}`, {
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
| `category` | string | no | Optional category or comma-separated categories returned by List Fact Categories. |
| `name` | string | no | Optional name used to personalize the returned fact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        "string"
      ],
      "created_at": "string",
      "icon_url": "https://example.com",
      "id": "string",
      "updated_at": "string",
      "url": "https://example.com",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | array<string> | Categories assigned to the fact. |
| `created_at` | string | Provider creation timestamp. |
| `icon_url` | string | Provider icon URL. |
| `id` | string | Provider fact identifier. |
| `updated_at` | string | Provider update timestamp. |
| `url` | string | Provider fact URL. |
| `value` | string | Fact text. |

## Native endpoint

Through the native Chuck Norris API, this operation is `GET /jokes/random` (base URL `https://api.chucknorris.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-fact.md) for the provider-specific parameters and requirements.

