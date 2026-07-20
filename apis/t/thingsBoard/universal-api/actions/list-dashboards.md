# ThingsBoard: List Dashboards

Retrieves dashboard info records from ThingsBoard.

```
GET https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/list-dashboards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThingsBoard `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/list-dashboards?connectionId=$CONNECTION_ID&limit=25&offset=0&pageSize=1&page=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "pageSize": "1",
  "page": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/list-dashboards?${params}`, {
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
| `pageSize` | number | yes | Maximum number of dashboard records to return in one page. |
| `page` | number | yes | Zero-based page number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "createdTime": 1,
          "id": {
            "entityType": "string",
            "id": "string"
          },
          "image": "string",
          "mobileHide": true,
          "mobileOrder": 1,
          "name": "Ava Chen",
          "title": "string",
          "version": 1
        }
      ],
      "hasNext": true,
      "totalElements": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].createdTime` | number |  |
| `data[].id.entityType` | string |  |
| `data[].id.id` | string |  |
| `data[].image` | string |  |
| `data[].mobileHide` | boolean |  |
| `data[].mobileOrder` | number |  |
| `data[].name` | string |  |
| `data[].title` | string |  |
| `data[].version` | number |  |
| `hasNext` | boolean |  |
| `totalElements` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native ThingsBoard API, this operation is `GET /tenant/dashboards` (base URL `{{credentials.baseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-dashboards.md) for the provider-specific parameters and requirements.

