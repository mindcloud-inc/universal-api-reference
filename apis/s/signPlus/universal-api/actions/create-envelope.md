# Sign.Plus: Create Envelope



```
POST https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/create-envelope
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sign.Plus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/create-envelope" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "flowType": "string",
  "legalityLevel": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/create-envelope', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "flowType": "string",
    "legalityLevel": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Envelope name |
| `flowType` | string | yes | Envelope flow type |
| `legalityLevel` | string | yes | Envelope legality level |
| `expiresAt` | number | no | Unix timestamp for envelope expiration |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": {},
      "comment": "string",
      "created_at": 1,
      "documents": [
        {}
      ],
      "expires_at": 1,
      "flow_type": "string",
      "id": "string",
      "is_duplicable": true,
      "legality_level": "string",
      "name": "Ava Chen",
      "notification": {},
      "num_recipients": 1,
      "pages": 1,
      "signing_steps": [
        {}
      ],
      "status": "string",
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | object |  |
| `comment` | string |  |
| `created_at` | number |  |
| `documents` | array<object> |  |
| `expires_at` | number |  |
| `flow_type` | string |  |
| `id` | string |  |
| `is_duplicable` | boolean |  |
| `legality_level` | string |  |
| `name` | string |  |
| `notification` | object |  |
| `num_recipients` | number |  |
| `pages` | number |  |
| `signing_steps` | array<object> |  |
| `status` | string |  |
| `updated_at` | number |  |

## Native endpoint

Through the native Sign.Plus API, this operation is `POST /envelope` (base URL `https://restapi.sign.plus/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-envelope.md) for the provider-specific parameters and requirements.

