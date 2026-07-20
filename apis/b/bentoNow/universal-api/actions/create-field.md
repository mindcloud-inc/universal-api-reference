# Bento Now: Create Field

Creates a custom profile field in Bento Now.

```
POST https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/create-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bento Now `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/create-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/create-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "key": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `key` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "key": "string",
        "name": "Ava Chen",
        "whitelisted": {}
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.createdAt` | date |  |
| `attributes.key` | string |  |
| `attributes.name` | string |  |
| `attributes.whitelisted` | object |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Bento Now API, this operation is `POST /v1/fetch/fields` (base URL `https://app.bentonow.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-field.md) for the provider-specific parameters and requirements.

