# Certifier: Create Credential Interaction

Creates a credential interaction in Certifier.

```
POST https://connect.mindcloud.co/v1/universal/certifier/latest/actions/create-credential-interaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/certifier/latest/actions/create-credential-interaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "credentialId": "string",
  "eventType": "string",
  "triggeredBy": "string",
  "triggeredAt": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/certifier/latest/actions/create-credential-interaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "credentialId": "string",
    "eventType": "string",
    "triggeredBy": "string",
    "triggeredAt": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `credentialId` | string | yes |  |
| `eventType` | string | yes | Use one of Certifier's documented interaction event values. |
| `triggeredBy` | string | yes | Use recipient or guest. |
| `triggeredAt` | date | yes | Use an ISO 8601 date-time string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credentialId": "string",
      "eventType": "string",
      "id": "string",
      "triggeredAt": "2026-05-07T12:00:00.000Z",
      "triggeredBy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credentialId` | string |  |
| `eventType` | string |  |
| `id` | string |  |
| `triggeredAt` | date |  |
| `triggeredBy` | string |  |

## Native endpoint

Through the native Certifier API, this operation is `POST /credential-interactions` (base URL `https://api.certifier.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-credential-interaction.md) for the provider-specific parameters and requirements.

