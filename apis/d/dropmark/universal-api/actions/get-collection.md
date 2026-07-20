# Dropmark: Get Collection



```
GET https://connect.mindcloud.co/v1/universal/dropmark/latest/actions/get-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropmark/latest/actions/get-collection?connectionId=$CONNECTION_ID&collectionId=1&collectionKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "1",
  "collectionKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropmark/latest/actions/get-collection?${params}`, {
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
| `collectionId` | number | yes | Numeric Dropmark collection identifier. |
| `collectionKey` | string | yes | Collection-specific read-only key from Collection Settings > Advanced > JSON. Required for private collections unless you use basic auth outside this app contract. |
| `callback` | string | no | Optional JSONP callback name supported by Dropmark collection JSON feeds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": 1,
      "items": [
        {}
      ],
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
| `description` | string | Collection description. |
| `id` | number | Collection identifier. |
| `items` | array<object> | Items returned in the collection payload when present. |
| `name` | string | Collection name. |
| `url` | string | Collection URL. |

## Native endpoint

Through the native Dropmark API, this operation is `GET /{{args.collectionId}}.json` (base URL `https://{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-collection.md) for the provider-specific parameters and requirements.

