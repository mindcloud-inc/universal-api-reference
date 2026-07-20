# Bookvault: List Publishers

Retrieves publishers from your Bookvault account.

```
GET https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-publishers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookvault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-publishers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-publishers?${params}`, {
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
      "CityOfPublication": "string",
      "CountryOfPublication": "string",
      "CountryOfPublicationID": 1,
      "PublisherID": 1,
      "PublisherName": "Ava Chen",
      "Websites": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CityOfPublication` | string |  |
| `CountryOfPublication` | string |  |
| `CountryOfPublicationID` | number |  |
| `PublisherID` | number |  |
| `PublisherName` | string |  |
| `Websites` | array<object> |  |

## Native endpoint

Through the native Bookvault API, this operation is `GET /Publisher` (base URL `https://api.bookvault.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-publishers.md) for the provider-specific parameters and requirements.

