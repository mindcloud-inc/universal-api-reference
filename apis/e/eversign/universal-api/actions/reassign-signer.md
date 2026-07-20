# Eversign: Reassign Signer

Reassigns a signer on a document in Eversign.

```
PUT https://connect.mindcloud.co/v1/universal/eversign/latest/actions/reassign-signer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eversign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eversign/latest/actions/reassign-signer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentHash": "string",
  "signerId": "string",
  "newSignerName": "Ava Chen",
  "newSignerEmail": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eversign/latest/actions/reassign-signer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentHash": "string",
    "signerId": "string",
    "newSignerName": "Ava Chen",
    "newSignerEmail": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentHash` | string | yes |  |
| `signerId` | string | yes |  |
| `newSignerName` | string | yes |  |
| `newSignerEmail` | string | yes |  |
| `reason` | string | no |  |

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
| `success` | boolean |  |

## Native endpoint

Through the native Eversign API, this operation is `POST /reassign` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reassign-signer.md) for the provider-specific parameters and requirements.

