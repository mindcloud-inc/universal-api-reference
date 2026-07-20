# GraphHopper: Create Custom Routing Profile

Creates a custom routing profile in GraphHopper.

```
POST https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/create-custom-routing-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GraphHopper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/create-custom-routing-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requestBody": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/create-custom-routing-profile', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requestBody": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requestBody` | object | yes | Custom routing profile request JSON body matching GraphHopper's ProfileRequest schema. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounds": {},
      "custom_model": {},
      "id": "string",
      "profile": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounds` | object | Profile bounds. |
| `custom_model` | object | Custom model. |
| `id` | string | Custom profile ID. |
| `profile` | string | Custom profile name. |

## Native endpoint

Through the native GraphHopper API, this operation is `POST /profiles` (base URL `https://graphhopper.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-routing-profile.md) for the provider-specific parameters and requirements.

