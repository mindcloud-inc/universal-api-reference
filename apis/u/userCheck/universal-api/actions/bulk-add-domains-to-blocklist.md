# UserCheck: Bulk Add Domains to Blocklist

Adds multiple domains to the UserCheck blocklist.

```
POST https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/bulk-add-domains-to-blocklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UserCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/bulk-add-domains-to-blocklist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domains[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/bulk-add-domains-to-blocklist', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domains[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domains[]` | array<string> | yes | Domains to add to the blocklist. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {}
      ],
      "failed": 1,
      "succeeded": 1,
      "success": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<object> |  |
| `failed` | number |  |
| `succeeded` | number |  |
| `success` | array<object> |  |

## Native endpoint

Through the native UserCheck API, this operation is `POST /blocklist/bulk` (base URL `https://api.usercheck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-add-domains-to-blocklist.md) for the provider-specific parameters and requirements.

