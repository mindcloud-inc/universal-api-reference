# Modusign: Update Current Signing Turn Expiration

Updates the current signing turn expiration in Modusign.

```
PUT https://connect.mindcloud.co/v1/universal/modusign/latest/actions/update-current-signing-turn-expiration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/modusign/latest/actions/update-current-signing-turn-expiration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datetime": "string",
  "documentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/modusign/latest/actions/update-current-signing-turn-expiration', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datetime": "string",
    "documentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datetime` | string | yes | The new ISO datetime for the current signing turn expiration. |
| `documentId` | string | yes | The Modusign document ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the signing turn expiration was successfully updated. |

## Native endpoint

Through the native Modusign API, this operation is `PUT /documents/:documentId/change-signing-due` (base URL `https://api.modusign.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-current-signing-turn-expiration.md) for the provider-specific parameters and requirements.

