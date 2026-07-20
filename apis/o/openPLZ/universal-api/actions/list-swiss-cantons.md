# OpenPLZ: List Swiss Cantons



```
GET https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/list-swiss-cantons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenPLZ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/list-swiss-cantons?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/list-swiss-cantons?${params}`, {
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
      "historicalCode": "string",
      "key": "string",
      "name": "Ava Chen",
      "shortName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `historicalCode` | string |  |
| `key` | string |  |
| `name` | string |  |
| `shortName` | string |  |

## Native endpoint

Through the native OpenPLZ API, this operation is `GET /ch/Cantons` (base URL `https://openplzapi.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-swiss-cantons.md) for the provider-specific parameters and requirements.

