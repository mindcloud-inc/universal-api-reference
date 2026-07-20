# Verix: Update Multiple Credentials

Updates multiple credentials in Verix for a group.

```
PUT https://connect.mindcloud.co/v1/universal/verix/latest/actions/update-multiple-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/verix/latest/actions/update-multiple-credentials" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "group_id": "894",
  "inputs[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/verix/latest/actions/update-multiple-credentials', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "group_id": "894",
    "inputs[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `group_id` | number | yes | Target Verix group ID for credential updates. Example: `894`. |
| `inputs[]` | array<object> | yes | Array of credential update payloads. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {}
      ],
      "requestId": 1,
      "updated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<object> | Credential update errors returned by Verix. |
| `requestId` | number | Asynchronous Verix request identifier. |
| `updated` | number | Number of credentials updated. |

## Native endpoint

Through the native Verix API, this operation is `PUT /v1/credentials/groups/:group_id/` (base URL `https://api.verix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-multiple-credentials.md) for the provider-specific parameters and requirements.

