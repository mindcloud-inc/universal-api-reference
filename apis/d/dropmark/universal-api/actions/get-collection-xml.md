# Dropmark: Get Collection XML



```
GET https://connect.mindcloud.co/v1/universal/dropmark/latest/actions/get-collection-xml
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropmark/latest/actions/get-collection-xml?connectionId=$CONNECTION_ID&collectionId=1&collectionKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "1",
  "collectionKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropmark/latest/actions/get-collection-xml?${params}`, {
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
| `collectionKey` | string | yes | Collection-specific read-only key from Collection Settings > Advanced > JSON. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "format": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Raw XML document returned by the collection feed. |
| `format` | string | Feed format identifier. |

## Native endpoint

Through the native Dropmark API, this operation is `GET /{{args.collectionId}}.xml` (base URL `https://{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-collection-xml.md) for the provider-specific parameters and requirements.

