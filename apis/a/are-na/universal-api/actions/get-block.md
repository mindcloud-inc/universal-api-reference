# Are.na: Get Block

Retrieves a block by ID from Are.na.

```
GET https://connect.mindcloud.co/v1/universal/are-na/latest/actions/get-block
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Are.na `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/are-na/latest/actions/get-block?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/are-na/latest/actions/get-block?${params}`, {
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
| `id` | string | no | Are.na block ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "content": {},
      "id": 1,
      "source": {},
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object |  |
| `content` | object |  |
| `id` | number |  |
| `source` | object |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Are.na API, this operation is `GET blocks/:id` (base URL `https://api.are.na/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-block.md) for the provider-specific parameters and requirements.

