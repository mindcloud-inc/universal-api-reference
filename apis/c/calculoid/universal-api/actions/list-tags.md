# Calculoid: List Tags



```
GET https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calculoid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/list-tags?connectionId=$CONNECTION_ID&limit=10&search=calculator" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "limit": "10",
  "search": "calculator"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/list-tags?${params}`, {
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
| `limit` | number | yes | Maximum number of tags to return. Default: `10`. Example: `10`. |
| `search` | string | yes | Tag search text. Default: `calculator`. Example: `calculator`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | string |  |

## Native endpoint

Through the native Calculoid API, this operation is `GET /tags/:limit/:search` (base URL `https://api.calculoid.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

