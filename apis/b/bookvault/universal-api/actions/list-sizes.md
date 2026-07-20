# Bookvault: List Sizes

Retrieves available book sizes from Bookvault.

```
GET https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-sizes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookvault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-sizes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-sizes?${params}`, {
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
      "FixedSizing": true,
      "SizeHeight": 1,
      "SizeID": 1,
      "SizeName": "Ava Chen",
      "SizeWidth": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `FixedSizing` | boolean |  |
| `SizeHeight` | number |  |
| `SizeID` | number |  |
| `SizeName` | string |  |
| `SizeWidth` | number |  |

## Native endpoint

Through the native Bookvault API, this operation is `GET /Sizing` (base URL `https://api.bookvault.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sizes.md) for the provider-specific parameters and requirements.

