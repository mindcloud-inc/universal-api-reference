# Xata: Create an Organization API Key



```
POST https://connect.mindcloud.co/v1/universal/xata/latest/actions/create-organization-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xata/latest/actions/create-organization-api-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "organizationID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xata/latest/actions/create-organization-api-key', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "organizationID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `expiry` | string | no | Expiration date for the API key, null for no expiry |
| `scopes[]` | array | no | Optional scopes assigned to the API key |
| `scopes[]` | array | no | Optional scopes assigned to the API key |
| `projects[]` | array | no | Limit access to these projects |
| `projects[]` | array | no | Limit access to these projects |
| `branches[]` | array | no | Limit access to these branches |
| `branches[]` | array | no | Limit access to these branches |
| `organizationID` | string | yes | Unique identifier for a specific organization |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | object |  |

## Native endpoint

Through the native Xata API, this operation is `POST /organizations/:organizationID/api-keys` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-organization-api-key.md) for the provider-specific parameters and requirements.

