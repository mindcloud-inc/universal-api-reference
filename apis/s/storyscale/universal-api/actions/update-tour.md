# Storyscale: Update Tour



```
PUT https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/update-tour
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storyscale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/update-tour" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/update-tour', {
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
| `conversionEnabled` | boolean | no | Whether conversion tracking is enabled for the tour. |
| `description` | string | no | Updated description of the tour. |
| `id` | string | yes | The Storyscale tour ID. |
| `image` | string | no | Image for the tour. |
| `isActive` | boolean | no | Whether the tour is active. |
| `isPublished` | boolean | no | Whether the tour is published. |
| `isResponsiveTourEnabled` | boolean | no | Whether responsive tour behavior is enabled. |
| `isTemplate` | boolean | no | Whether the tour is a template. |
| `name` | string | no | Updated name of the tour. |
| `styleGuideId` | number | no | Style guide to associate with the tour. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Updated tour payload returned by Storyscale. |
| `status` | object | Top-level API status object. |

## Native endpoint

Through the native Storyscale API, this operation is `PUT /v1/tour/update/{id}` (base URL `https://prodapi.storyscale.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tour.md) for the provider-specific parameters and requirements.

