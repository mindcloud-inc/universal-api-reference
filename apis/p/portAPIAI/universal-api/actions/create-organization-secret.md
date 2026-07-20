# Port API AI: Create Organization Secret

Creates an organization secret in Port.

```
POST https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-organization-secret
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-organization-secret" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "secretName": "Ava Chen",
  "secretValue": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-organization-secret', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "secretName": "Ava Chen",
    "secretValue": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `secretName` | string | yes | The organization secret name. |
| `secretValue` | string | yes | The organization secret value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true,
      "secret": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |
| `secret` | object |  |

## Native endpoint

Through the native Port API AI API, this operation is `POST /organization/secrets` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-organization-secret.md) for the provider-specific parameters and requirements.

