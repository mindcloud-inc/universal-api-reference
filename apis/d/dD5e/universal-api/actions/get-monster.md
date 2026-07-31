# D&D 5e: Get Monster



```
GET https://connect.mindcloud.co/v1/universal/dD5e/latest/actions/get-monster
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D&D 5e `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dD5e/latest/actions/get-monster?connectionId=$CONNECTION_ID&index=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "index": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dD5e/latest/actions/get-monster?${params}`, {
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
| `index` | string | yes | Monster index. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "desc": [
        "string"
      ],
      "index": "string",
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `desc` | array<string> |  |
| `index` | string |  |
| `name` | string |  |
| `url` | string |  |

## Native endpoint

Through the native D&D 5e API, this operation is `GET /monsters/:index` (base URL `https://www.dnd5eapi.co/api/2014`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-monster.md) for the provider-specific parameters and requirements.

