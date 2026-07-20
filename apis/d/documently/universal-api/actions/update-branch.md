# Documently: Update Branch

Updates an existing branch in Documently.

```
PUT https://connect.mindcloud.co/v1/universal/documently/latest/actions/update-branch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/documently/latest/actions/update-branch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "branchId": "string",
  "name": "Ava Chen",
  "project": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documently/latest/actions/update-branch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "branchId": "string",
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
| `branchId` | string | yes |  |
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

Through the native Documently API, this operation is `PATCH /branches/:branchId` (base URL `https://app.documently.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-branch.md) for the provider-specific parameters and requirements.

