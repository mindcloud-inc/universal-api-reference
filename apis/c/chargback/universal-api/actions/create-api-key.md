# Chargback: Create API Key

Creates a new API key in Chargback.

```
POST https://connect.mindcloud.co/v1/universal/chargback/latest/actions/create-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargback `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chargback/latest/actions/create-api-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "platform": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chargback/latest/actions/create-api-key', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "platform": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `platform` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "key": "string",
      "platform": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string | API key creation timestamp. |
| `key` | string | Created API key value returned once by Chargeback. |
| `platform` | string | Platform for the created API key. |
| `updated` | string | API key last update timestamp. |

## Native endpoint

Through the native Chargback API, this operation is `POST /api/public/v1/api-keys/` (base URL `https://api.chargeback.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-api-key.md) for the provider-specific parameters and requirements.

