# Bookvault: List Collections

Retrieves available collections from Bookvault.

```
GET https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookvault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-collections?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "CollectionID": 1,
      "Description": "string",
      "Image": "string",
      "Name": "Ava Chen",
      "ShopifyID": 1,
      "Uploaded": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CollectionID` | number |  |
| `Description` | string |  |
| `Image` | string |  |
| `Name` | string |  |
| `ShopifyID` | number |  |
| `Uploaded` | boolean |  |

## Native endpoint

Through the native Bookvault API, this operation is `GET /Collections` (base URL `https://api.bookvault.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-collections.md) for the provider-specific parameters and requirements.

