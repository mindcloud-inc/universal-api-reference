# Xola: Create Experience

Creates a new experience in Xola.

```
POST https://connect.mindcloud.co/v1/universal/xola/latest/actions/create-experience
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xola `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xola/latest/actions/create-experience" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "demographics": "string",
  "desc": "string",
  "duration": "string",
  "excerpt": "string",
  "name": "Ava Chen",
  "priceSchemes": "string",
  "seller": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xola/latest/actions/create-experience', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "demographics": "string",
    "desc": "string",
    "duration": "string",
    "excerpt": "string",
    "name": "Ava Chen",
    "priceSchemes": "string",
    "seller": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `demographics` | string | yes |  |
| `desc` | string | yes |  |
| `duration` | string | yes |  |
| `excerpt` | string | yes |  |
| `name` | string | yes |  |
| `priceSchemes` | string | yes |  |
| `seller` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "seller": {
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Experience identifier. |
| `name` | string | Experience name. |
| `object` | string | Xola object type. |
| `seller.id` | string | Owning seller identifier. |

## Native endpoint

Through the native Xola API, this operation is `POST /experiences` (base URL `https://sandbox.xola.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-experience.md) for the provider-specific parameters and requirements.

