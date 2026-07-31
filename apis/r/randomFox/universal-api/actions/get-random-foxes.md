# RandomFox: Get Random Foxes



```
GET https://connect.mindcloud.co/v1/universal/randomFox/latest/actions/get-random-foxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RandomFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/randomFox/latest/actions/get-random-foxes?connectionId=$CONNECTION_ID&count=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "count": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/randomFox/latest/actions/get-random-foxes?${params}`, {
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
| `count` | number | yes | Number of unique foxes to return (1–20). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "images": [
        "string"
      ],
      "links": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `images` | array<string> | Direct URLs of the returned random fox images. |
| `links` | array<string> | RandomFox page URLs corresponding to the returned images. |

## Native endpoint

Through the native RandomFox API, this operation is `GET /api/v1/getfoxes/` (base URL `https://randomfox.ca`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-foxes.md) for the provider-specific parameters and requirements.

