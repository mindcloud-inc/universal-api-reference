# UserCheck: Add Domain to Blocklist

Adds a domain to the UserCheck blocklist.

```
POST https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/add-domain-to-blocklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UserCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/add-domain-to-blocklist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/add-domain-to-blocklist', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | yes | Domain to add to the blocklist. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "domain": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `domain` | string |  |

## Native endpoint

Through the native UserCheck API, this operation is `POST /blocklist` (base URL `https://api.usercheck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-domain-to-blocklist.md) for the provider-specific parameters and requirements.

