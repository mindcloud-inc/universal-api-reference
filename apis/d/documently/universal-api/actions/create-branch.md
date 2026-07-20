# Documently: Create Branch

Creates a new branch in Documently.

```
POST https://connect.mindcloud.co/v1/universal/documently/latest/actions/create-branch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documently/latest/actions/create-branch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "project": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documently/latest/actions/create-branch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "project": "string",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `project` | string | yes |  |
| `status` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "author": {},
      "id": "string",
      "name": "Ava Chen",
      "project": "string",
      "sortOrder": [
        "string"
      ],
      "status": "string",
      "storageToBeDeleted": [
        "string"
      ],
      "toBeDeleted": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@context` | string |  |
| `@id` | string |  |
| `@type` | string |  |
| `author` | object |  |
| `id` | string |  |
| `name` | string |  |
| `project` | string |  |
| `sortOrder` | array<string> |  |
| `status` | string |  |
| `storageToBeDeleted` | array<string> |  |
| `toBeDeleted` | array<string> |  |

## Native endpoint

Through the native Documently API, this operation is `POST /branches` (base URL `https://app.documently.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-branch.md) for the provider-specific parameters and requirements.

