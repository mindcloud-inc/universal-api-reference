# FireHydrant: List Functionalities

Retrieves all functionality records from FireHydrant.

```
GET https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-functionalities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FireHydrant `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-functionalities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-functionalities?${params}`, {
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
| `impacted` | string | no | Filter by whether functionalities are impacted by active incidents. |
| `name` | string | no | Search functionalities by name. |
| `owner` | string | no | Filter by owning team ID. |
| `query` | string | no | Search functionalities by name or description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "alertOnAdd": true,
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "id": "string",
          "name": "Ava Chen",
          "serviceTier": 1,
          "slug": "string",
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
| `data[].alertOnAdd` | boolean |  |
| `data[].createdAt` | date |  |
| `data[].description` | string |  |
| `data[].id` | string |  |
| `data[].name` | string |  |
| `data[].serviceTier` | number |  |
| `data[].slug` | string |  |
| `data[].updatedAt` | date |  |
| `pagination.count` | number |  |
| `pagination.items` | number |  |
| `pagination.last` | number |  |
| `pagination.page` | number |  |
| `pagination.pages` | number |  |

## Native endpoint

Through the native FireHydrant API, this operation is `GET /functionalities` (base URL `https://api.firehydrant.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-functionalities.md) for the provider-specific parameters and requirements.

