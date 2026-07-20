# HoorayHR: Get Label

Retrieves a label record from HoorayHR.

```
GET https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/get-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoorayHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/get-label?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/get-label?${params}`, {
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
| `id` | number | yes | The label ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "documentCategoryId": 1,
      "id": 1,
      "name": {},
      "systemCategoryType": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workflowCategoryId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedAt` | date |  |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `documentCategoryId` | number |  |
| `id` | number |  |
| `name` | object |  |
| `systemCategoryType` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `workflowCategoryId` | number |  |

## Native endpoint

Through the native HoorayHR API, this operation is `GET /labels/:id` (base URL `https://api.hoorayhr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-label.md) for the provider-specific parameters and requirements.

