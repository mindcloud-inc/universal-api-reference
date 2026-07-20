# Sharetribe: Create Listing

Creates a new listing in Sharetribe.

```
POST https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/create-listing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sharetribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/create-listing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "authorId": "string",
  "state": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/create-listing', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "authorId": "string",
    "state": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Listing title. |
| `authorId` | string | yes | The ID of the marketplace user to whom the listing belongs. |
| `state` | string | yes | Initial listing state: published or pendingApproval. |
| `description` | string | no | Listing description. |
| `geolocation` | object | no | Listing latitude and longitude object. |
| `price` | object | no | Listing money object with amount and currency. |
| `availabilityPlan` | object | no | Listing availability plan object. |
| `publicData` | object | no | Listing public extended data object. |
| `privateData` | object | no | Listing private extended data object. |
| `metadata` | object | no | Listing public metadata object. |
| `images[]` | array<string> | no | Ordered list of uploaded image IDs for the listing. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Resource attributes payload. |
| `id` | string | Resource ID. |
| `relationships` | object | Resource relationships payload. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Sharetribe API, this operation is `POST listings/create` (base URL `https://flex-integ-api.sharetribe.com/v1/integration_api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-listing.md) for the provider-specific parameters and requirements.

