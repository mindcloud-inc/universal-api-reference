# Oboloo: List Contract Types

Retrieves contract types from Oboloo.

```
GET https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/list-contract-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oboloo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/list-contract-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/list-contract-types?${params}`, {
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
| `search` | string | no | Filter contract types by name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": 1,
      "creator": {
        "documentId": {},
        "id": 1,
        "name": "Ava Chen",
        "userImage": {}
      },
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "status": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy` | number |  |
| `creator.documentId` | object |  |
| `creator.id` | number |  |
| `creator.name` | string |  |
| `creator.userImage` | object |  |
| `deletedAt` | date |  |
| `id` | number |  |
| `name` | string |  |
| `status` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Oboloo API, this operation is `GET /configuration/contract-type-list` (base URL `https://mindcloudwizard20260330.oboloo.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contract-types.md) for the provider-specific parameters and requirements.

