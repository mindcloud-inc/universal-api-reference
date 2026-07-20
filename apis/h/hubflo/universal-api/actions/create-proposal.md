# Hubflo: Create Proposal

Creates a draft proposal in Hubflo.

```
POST https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/create-proposal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hubflo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/create-proposal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/create-proposal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes |  |
| `description` | string | no |  |
| `quoteComment` | string | no |  |
| `userId` | string | yes |  |
| `projectId` | string | no |  |
| `expiresInDays` | number | no |  |
| `paymentTerms` | string | no |  |
| `contactIds` | list<string> | no |  |
| `paymentMethods` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "refusal_context": "string",
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `description` | string |  |
| `id` | string |  |
| `refusal_context` | string |  |
| `status` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Hubflo API, this operation is `POST /proposals` (base URL `https://app.hubflo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-proposal.md) for the provider-specific parameters and requirements.

