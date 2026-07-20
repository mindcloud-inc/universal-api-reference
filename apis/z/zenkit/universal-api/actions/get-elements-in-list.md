# Zenkit: Get Elements In List

Retrieves custom fields from a Zenkit list.

```
GET https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-elements-in-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-elements-in-list?connectionId=$CONNECTION_ID&listAllId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listAllId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-elements-in-list?${params}`, {
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
| `listAllId` | string | yes | The list all id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "deprecated_at": "string",
      "description": "string",
      "displayName": "Ava Chen",
      "elementcategory": 1,
      "id": 1,
      "isAutoCreated": true,
      "isPrimary": true,
      "listId": 1,
      "name": "Ava Chen",
      "resourceRole": "string",
      "shortId": "string",
      "sortOrder": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `deprecated_at` | string |  |
| `description` | string |  |
| `displayName` | string |  |
| `elementcategory` | number |  |
| `id` | number |  |
| `isAutoCreated` | boolean |  |
| `isPrimary` | boolean |  |
| `listId` | number |  |
| `name` | string |  |
| `resourceRole` | string |  |
| `shortId` | string |  |
| `sortOrder` | number |  |
| `updated_at` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Zenkit API, this operation is `GET /lists/:listAllId/elements` (base URL `https://zenkit.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-elements-in-list.md) for the provider-specific parameters and requirements.

