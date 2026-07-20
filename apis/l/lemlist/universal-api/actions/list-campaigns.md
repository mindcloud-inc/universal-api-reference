# lemlist: List Campaigns

Retrieves your campaign list from lemlist.

```
GET https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lemlist `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/list-campaigns?${params}`, {
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
| `status` | list | no | Filter campaigns by status. One of: `archived`, `draft`, `out_of_credits`, `paused`, `running`. Example: `running`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaigns": [
        {
          "createdAt": "string",
          "createdBy": "string",
          "id": "string",
          "name": "Ava Chen",
          "sequenceId": "string",
          "status": "string"
        }
      ],
      "pagination": {
        "currentPage": 1,
        "nextPage": 1,
        "totalPage": 1,
        "totalRecords": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaigns` | array<object> |  |
| `campaigns[].createdAt` | string |  |
| `campaigns[].createdBy` | string |  |
| `campaigns[].id` | string |  |
| `campaigns[].name` | string |  |
| `campaigns[].sequenceId` | string |  |
| `campaigns[].status` | string |  |
| `pagination` | object |  |
| `pagination.currentPage` | number |  |
| `pagination.nextPage` | number |  |
| `pagination.totalPage` | number |  |
| `pagination.totalRecords` | number |  |

## Native endpoint

Through the native lemlist API, this operation is `GET /campaigns` (base URL `https://api.lemlist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

