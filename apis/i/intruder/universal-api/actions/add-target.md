# Intruder: Add Target



```
POST https://connect.mindcloud.co/v1/universal/intruder/latest/actions/add-target
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intruder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intruder/latest/actions/add-target" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intruder/latest/actions/add-target', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | yes | Target address or CIDR. |
| `tags[]` | array<string> | no | Tag names to add to the target. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "displayAddress": "string",
      "hasApiSchemas": true,
      "hasAuthentications": true,
      "id": 1,
      "licenseType": "string",
      "tags": [
        "string"
      ],
      "targetStatus": "string",
      "targetType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `displayAddress` | string |  |
| `hasApiSchemas` | boolean |  |
| `hasAuthentications` | boolean |  |
| `id` | number |  |
| `licenseType` | string |  |
| `tags` | array<string> |  |
| `targetStatus` | string |  |
| `targetType` | string |  |

## Native endpoint

Through the native Intruder API, this operation is `POST /targets/` (base URL `https://api.intruder.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-target.md) for the provider-specific parameters and requirements.

