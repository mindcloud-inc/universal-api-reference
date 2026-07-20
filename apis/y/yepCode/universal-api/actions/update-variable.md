# YepCode: Update variable

Updates an existing variable in YepCode.

```
PUT https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/update-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YepCode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/update-variable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/update-variable', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique identifier of the variable to update. |
| `key` | string | no | Updated variable key or name. |
| `value` | string | no | Updated variable value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "id": "string",
      "isSensitive": true,
      "key": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Timestamp when the variable was created |
| `createdBy` | string | Username of the user who created the variable |
| `id` | string | Unique identifier (UUID) of the team variable |
| `isSensitive` | boolean | Whether the variable is marked as sensitive |
| `key` | string | Variable key used in processes |
| `value` | string | Variable value |

## Native endpoint

Through the native YepCode API, this operation is `PATCH /variables/:id` (base URL `https://cloud.yepcode.io/api/{{credentials.team}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-variable.md) for the provider-specific parameters and requirements.

