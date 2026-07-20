# Localazy: Update Source Key

Updates an existing source key in Localazy.

```
PUT https://connect.mindcloud.co/v1/universal/localazy/latest/actions/update-source-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Localazy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/localazy/latest/actions/update-source-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "keyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/localazy/latest/actions/update-source-key', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "keyId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Localazy project id or slug. |
| `keyId` | string | yes | Source key identifier. |
| `hidden` | boolean | no | Hide the key from translation in Localazy. |
| `comment` | string | no | Comment for translators. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deprecated` | number | no | Set to -1 to remove deprecation or to 0+ to mark the key deprecated. |
| `limit` | number | no | Translation character limit or -1 to disable. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | boolean | Whether the source key was updated successfully. |

## Native endpoint

Through the native Localazy API, this operation is `PUT /projects/:projectId/keys/:keyId` (base URL `https://api.localazy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-source-key.md) for the provider-specific parameters and requirements.

