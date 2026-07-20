# Bookvault: List Imprints

Retrieves imprints from your Bookvault account.

```
GET https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-imprints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookvault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-imprints?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-imprints?${params}`, {
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
      "ID": 1,
      "LinkedList": "https://example.com",
      "ListType": "string",
      "Value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ID` | number |  |
| `LinkedList` | string |  |
| `ListType` | string |  |
| `Value` | string |  |

## Native endpoint

Through the native Bookvault API, this operation is `GET /Imprint` (base URL `https://api.bookvault.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-imprints.md) for the provider-specific parameters and requirements.

