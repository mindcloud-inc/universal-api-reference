# Podscan: Get Publisher

Retrieves a publisher record from Podscan.

```
GET https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-publisher
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-publisher?connectionId=$CONNECTION_ID&publisherId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publisherId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-publisher?${params}`, {
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
| `publisherId` | string | yes | The publisher ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "podcasts": [
        {}
      ],
      "publisher": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `podcasts` | array<object> |  |
| `publisher` | object |  |

## Native endpoint

Through the native Podscan API, this operation is `GET /publishers/{publisherId}` (base URL `https://podscan.fm/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-publisher.md) for the provider-specific parameters and requirements.

