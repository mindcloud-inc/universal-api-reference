# Tinybird: Create Environment Variable



```
POST https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/create-environment-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tinybird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/create-environment-variable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/create-environment-variable', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The environment variable name. |
| `type` | string | no | Optional variable type; Tinybird defaults to secret. |
| `value` | string | yes | The value to store. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "edited_by": "string",
      "name": "Ava Chen",
      "type": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `edited_by` | string |  |
| `name` | string |  |
| `type` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Tinybird API, this operation is `POST v0/variables` (base URL `{{credentials.apiHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-environment-variable.md) for the provider-specific parameters and requirements.

