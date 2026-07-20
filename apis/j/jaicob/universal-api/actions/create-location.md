# Jaicob: Create Location



```
POST https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/create-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jaicob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/create-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/create-location', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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

Through the native Jaicob API, this operation is `POST /locations` (base URL `https://api.jaicob.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-location.md) for the provider-specific parameters and requirements.

