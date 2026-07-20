# Bookvault: List Countries

Retrieves available countries from Bookvault.

```
GET https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookvault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-countries?${params}`, {
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
      "EU": true,
      "Id": 1,
      "ISO_Code": "string",
      "Name": "Ava Chen",
      "RequiredPostcode": true,
      "Zone": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `EU` | boolean |  |
| `Id` | number |  |
| `ISO_Code` | string |  |
| `Name` | string |  |
| `RequiredPostcode` | boolean |  |
| `Zone` | object |  |

## Native endpoint

Through the native Bookvault API, this operation is `GET /Countries` (base URL `https://api.bookvault.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-countries.md) for the provider-specific parameters and requirements.

