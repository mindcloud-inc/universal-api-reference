# HotspotSystem: List Social Transactions by Location

Retrieves social transactions at a specific location from HotspotSystem.

```
GET https://connect.mindcloud.co/v1/universal/hotspotSystem/latest/actions/list-social-transactions-by-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HotspotSystem `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hotspotSystem/latest/actions/list-social-transactions-by-location?connectionId=$CONNECTION_ID&limit=25&offset=0&locationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "locationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hotspotSystem/latest/actions/list-social-transactions-by-location?${params}`, {
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
| `locationId` | string | yes | The ID of a location. |
| `fields` | string | no | Comma-separated list of response properties to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionDateGmt": "string",
      "address": "string",
      "city": "string",
      "companyName": "Ava Chen",
      "countryCode": "string",
      "customer": "string",
      "email": "ava@example.com",
      "id": 1,
      "locationId": 1,
      "newsletter": 1,
      "operator": "string",
      "packageId": "string",
      "phone": "string",
      "socialAgeRange": "string",
      "socialFollowersCount": "string",
      "socialGender": "string",
      "socialId": "string",
      "socialLink": "https://example.com",
      "socialNetwork": "string",
      "socialUsername": "Ava Chen",
      "state": "string",
      "userAgent": "string",
      "userName": "Ava Chen",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionDateGmt` | string |  |
| `address` | string |  |
| `city` | string |  |
| `companyName` | string |  |
| `countryCode` | string |  |
| `customer` | string |  |
| `email` | string |  |
| `id` | number |  |
| `locationId` | number |  |
| `newsletter` | number |  |
| `operator` | string |  |
| `packageId` | string |  |
| `phone` | string |  |
| `socialAgeRange` | string |  |
| `socialFollowersCount` | string |  |
| `socialGender` | string |  |
| `socialId` | string |  |
| `socialLink` | string |  |
| `socialNetwork` | string |  |
| `socialUsername` | string |  |
| `state` | string |  |
| `userAgent` | string |  |
| `userName` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native HotspotSystem API, this operation is `GET /locations/:locationId/transactions/social` (base URL `https://api.hotspotsystem.com/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-social-transactions-by-location.md) for the provider-specific parameters and requirements.

