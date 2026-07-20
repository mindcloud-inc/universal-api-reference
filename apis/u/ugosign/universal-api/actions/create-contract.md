# Ugosign: Create Contract

Creates a new contract in Ugosign.

```
POST https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/create-contract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ugosign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/create-contract" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "authorId": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/create-contract', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "authorId": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowRefusal` | boolean | no |  |
| `authorId` | string | yes |  |
| `content` | string | no |  |
| `description` | string | no |  |
| `file` | file | no |  |
| `folderId` | string | no |  |
| `footer` | string | no |  |
| `initials` | boolean | no |  |
| `reminder` | number | no |  |
| `title` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowRefusal": true,
      "authorId": "string",
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "folderId": "string",
      "footer": "string",
      "id": "string",
      "initials": true,
      "message": "string",
      "organizationId": "string",
      "reminder": 1,
      "title": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowRefusal` | boolean |  |
| `authorId` | string |  |
| `content` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `folderId` | string |  |
| `footer` | string |  |
| `id` | string |  |
| `initials` | boolean |  |
| `message` | string |  |
| `organizationId` | string |  |
| `reminder` | number |  |
| `title` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Ugosign API, this operation is `POST /v1/contracts` (base URL `https://app.ugosign.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contract.md) for the provider-specific parameters and requirements.

