# Keysender: Update Code

Updates an existing code in Keysender.

```
PUT https://connect.mindcloud.co/v1/universal/keysender/latest/actions/update-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keysender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/keysender/latest/actions/update-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keysender/latest/actions/update-code', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no |  |
| `sendfirst` | string | no |  |
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filename": "Ava Chen",
      "id": 1,
      "keyusage": 1,
      "sendfirst": 1,
      "status": 1,
      "type": 1,
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filename` | string | Stored filename for file codes. |
| `id` | number | Code identifier. |
| `keyusage` | number | Usage count. |
| `sendfirst` | number | Send-first flag. |
| `status` | number | Code usage status. |
| `type` | number | Code type. |
| `value` | string | Code value or filename. |

## Native endpoint

Through the native Keysender API, this operation is `PUT /code` (base URL `https://panel.keysender.co.uk/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-code.md) for the provider-specific parameters and requirements.

