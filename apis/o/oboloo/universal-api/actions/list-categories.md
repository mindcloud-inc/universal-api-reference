# Oboloo: List Categories

Retrieves categories from Oboloo.

```
GET https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/list-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oboloo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/list-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/list-categories?${params}`, {
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
| `search` | string | no | Filter categories by name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "creator": {},
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "status": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | object |  |
| `createdAt` | date |  |
| `createdBy` | object |  |
| `creator` | object |  |
| `deletedAt` | date |  |
| `id` | number |  |
| `status` | number |  |
| `updatedAt` | date |  |
| `value` | string |  |

## Native endpoint

Through the native Oboloo API, this operation is `GET /configuration/getCategories` (base URL `https://mindcloudwizard20260330.oboloo.app/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-categories.md) for the provider-specific parameters and requirements.

