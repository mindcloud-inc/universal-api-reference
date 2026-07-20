# Dropmark: Get Collection Export



```
GET https://connect.mindcloud.co/v1/universal/dropmark/latest/actions/get-collection-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropmark/latest/actions/get-collection-export?connectionId=$CONNECTION_ID&collectionId=1&format=0&collectionKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "1",
  "format": "0",
  "collectionKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropmark/latest/actions/get-collection-export?${params}`, {
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
| `format` | string | yes | Raw collection export representation. One of: `0`, `1`, `2`, `3`. |
| `collectionKey` | string | yes | Collection-specific read-only key from Collection Settings > Advanced > JSON. Required for private collections unless you use basic auth outside this app contract. |

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
| `content` | string | Raw collection export response body. |
| `format` | string | Requested export format. |

## Native endpoint

Through the native Dropmark API, this operation is `GET /{{args.collectionId}}.{{args.format}}` (base URL `https://{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-collection-export.md) for the provider-specific parameters and requirements.

