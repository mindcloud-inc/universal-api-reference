# Tremendous: Create Campaign

Creates a new campaign in Tremendous.

```
POST https://connect.mindcloud.co/v1/universal/tremendous/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tremendous `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tremendous/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "description": "string",
  "name": "Ava Chen",
  "products[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tremendous/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "description": "string",
    "name": "Ava Chen",
    "products[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | yes | Description of the campaign |
| `name` | string | yes | Name of the campaign |
| `products[]` | array<string> | yes | Product IDs available in the campaign |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | object |  |

## Native endpoint

Through the native Tremendous API, this operation is `POST /campaigns` (base URL `https://testflight.tremendous.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

