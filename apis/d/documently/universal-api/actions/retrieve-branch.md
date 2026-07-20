# Documently: Retrieve Branch

Retrieves a branch from Documently.

```
GET https://connect.mindcloud.co/v1/universal/documently/latest/actions/retrieve-branch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documently/latest/actions/retrieve-branch?connectionId=$CONNECTION_ID&branchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "branchId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documently/latest/actions/retrieve-branch?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `branchId` | string | yes |  |

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

Through the native Documently API, this operation is `GET /branches/:branchId` (base URL `https://app.documently.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-branch.md) for the provider-specific parameters and requirements.

