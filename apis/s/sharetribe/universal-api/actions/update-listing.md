# Sharetribe: Update Listing

Updates an existing listing in Sharetribe.

```
PUT https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/update-listing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sharetribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/update-listing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/update-listing', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the listing that is being updated. |
| `title` | string | no | Listing title. |
| `description` | string | no | Listing description. |
| `geolocation` | object | no | Listing latitude and longitude object. Pass null to remove. |
| `price` | object | no | Listing money object with amount and currency. Pass null to remove. |
| `availabilityPlan` | object | no | Full listing availability plan object. Pass null to reset to default daily availability. |
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

Through the native Sharetribe API, this operation is `POST listings/update` (base URL `https://flex-integ-api.sharetribe.com/v1/integration_api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-listing.md) for the provider-specific parameters and requirements.

