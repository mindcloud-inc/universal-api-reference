# Cryptolens: List Data Objects

Retrieves data objects from Cryptolens.

```
GET https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/list-data-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptolens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/list-data-objects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/list-data-objects?${params}`, {
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
      "id": 1,
      "intValue": 1,
      "name": "Ava Chen",
      "stringValue": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | List Data Objects response field `id` from Cryptolens docs example. |
| `intValue` | number | List Data Objects response field `intValue` from Cryptolens docs example. |
| `name` | string | List Data Objects response field `name` from Cryptolens docs example. |
| `stringValue` | string | List Data Objects response field `stringValue` from Cryptolens docs example. |

## Native endpoint

Through the native Cryptolens API, this operation is `GET /api/data/ListDataObjects` (base URL `https://api.cryptolens.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-data-objects.md) for the provider-specific parameters and requirements.

