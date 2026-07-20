# NiftyImages: Update Map Location

Updates an existing map location in NiftyImages.

```
PUT https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/update-map-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NiftyImages `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/update-map-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/update-map-location', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | NiftyImages map URL. |
| `NiftyID` | string | no | NiftyImages location ID to update. |
| `Address` | string | no | New address for the location. |
| `Latitude` | number | no | New latitude for the location. |
| `Longitude` | number | no | New longitude for the location. |
| `LocationID` | string | no | Location ID for the location. |
| `Properties[]` | array<object> | no | Optional properties to attach to the location. |
| `Properties[].Name` | string | no | Property name. |
| `Properties[].Value` | string | no | Property value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native NiftyImages API, this operation is `PUT /Maps/UpdateLocation` (base URL `https://api.niftyimages.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-map-location.md) for the provider-specific parameters and requirements.

