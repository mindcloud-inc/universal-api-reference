# Beds24: List Airbnb Listings

Retrieves Airbnb listings from Beds24 by Airbnb user ID.

```
GET https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-airbnb-listings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beds24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-airbnb-listings?connectionId=$CONNECTION_ID&airbnbUserId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "airbnbUserId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-airbnb-listings?${params}`, {
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
| `airbnbUserId` | string | yes | Connected Airbnb user ID to list listings for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "airbnbListing": {},
      "enabled": true,
      "name": "Ava Chen",
      "roomId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `airbnbListing` | object |  |
| `enabled` | boolean |  |
| `name` | string |  |
| `roomId` | number |  |

## Native endpoint

Through the native Beds24 API, this operation is `GET /channels/airbnb/listings` (base URL `https://beds24.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-airbnb-listings.md) for the provider-specific parameters and requirements.

