# FireHydrant: List Runbooks

Retrieves runbooks from FireHydrant.

```
GET https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-runbooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FireHydrant `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-runbooks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-runbooks?${params}`, {
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
| `name` | string | no | Filter runbooks by name. |
| `owners` | string | no | Filter runbooks by owner IDs. |
| `sort` | string | no | Sort order for runbooks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "categories": [
            "string"
          ],
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "id": "string",
          "name": "Ava Chen",
          "summary": "string",
          "type": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "pagination": {
        "count": 1,
        "items": 1,
        "last": 1,
        "page": 1,
        "pages": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].categories` | array<string> |  |
| `data[].createdAt` | date |  |
| `data[].description` | string |  |
| `data[].id` | string |  |
| `data[].name` | string |  |
| `data[].summary` | string |  |
| `data[].type` | string |  |
| `data[].updatedAt` | date |  |
| `pagination.count` | number |  |
| `pagination.items` | number |  |
| `pagination.last` | number |  |
| `pagination.page` | number |  |
| `pagination.pages` | number |  |

## Native endpoint

Through the native FireHydrant API, this operation is `GET /runbooks` (base URL `https://api.firehydrant.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-runbooks.md) for the provider-specific parameters and requirements.

