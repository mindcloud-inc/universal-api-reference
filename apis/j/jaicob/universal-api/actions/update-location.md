# Jaicob: Update Location



```
PUT https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/update-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jaicob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/update-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "addressLine1": "string",
  "postcode": "string",
  "city": "string",
  "country": "string",
  "state": "string",
  "isHeadQuarter": true,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/update-location', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "addressLine1": "string",
    "postcode": "string",
    "city": "string",
    "country": "string",
    "state": "string",
    "isHeadQuarter": true,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Location identifier. |
| `addressLine1` | string | yes |  |
| `addressLine2` | string | no |  |
| `email` | string | no |  |
| `phone` | string | no |  |
| `postcode` | string | yes |  |
| `city` | string | yes |  |
| `country` | string | yes |  |
| `state` | string | yes |  |
| `isHeadQuarter` | boolean | yes |  |
| `name` | string | yes |  |
| `clientId` | string | no |  |
| `vacancyIds[]` | array<string> | no |  |
| `userIds[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Jaicob API, this operation is `PUT /locations/[:id]` (base URL `https://api.jaicob.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-location.md) for the provider-specific parameters and requirements.

