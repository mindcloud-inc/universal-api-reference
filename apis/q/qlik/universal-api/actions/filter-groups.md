# Qlik: Filter Groups

Finds groups in Qlik by advanced filter query.

```
GET https://connect.mindcloud.co/v1/universal/qlik/latest/actions/filter-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/filter-groups?connectionId=$CONNECTION_ID&limit=25&offset=0&filter=name%20eq%20%22Analytics%20Team%22" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "filter": "name eq \"Analytics Team\""
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qlik/latest/actions/filter-groups?${params}`, {
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
| `filter` | string | yes | SCIM filter expression for matching groups. Example: `name eq "Analytics Team"`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "id": "string",
          "name": "Ava Chen",
          "status": "string",
          "tenantId": "string"
        }
      ],
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].id` | string |  |
| `data[].name` | string |  |
| `data[].status` | string |  |
| `data[].tenantId` | string |  |
| `totalResults` | number |  |

## Native endpoint

Through the native Qlik API, this operation is `POST /api/v1/groups/actions/filter` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/filter-groups.md) for the provider-specific parameters and requirements.

