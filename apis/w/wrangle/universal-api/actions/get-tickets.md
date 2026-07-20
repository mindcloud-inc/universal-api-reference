# Wrangle: Get Tickets



```
GET https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/get-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrangle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/get-tickets?connectionId=$CONNECTION_ID&inboxId=inbox_uuid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inboxId": "inbox_uuid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/get-tickets?${params}`, {
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
| `inboxId` | string | yes | The Wrangle inbox ID. Example: `inbox_uuid`. |
| `page` | number | no | Page number for pagination (1-based). Defaults to 1. Default: `1`. |
| `pageSize` | number | no | Number of tickets per page. Maximum 200. Defaults to 200. Default: `200`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "page": 1,
        "pageSize": 1,
        "totalCount": 1,
        "totalPages": 1
      },
      "success": true,
      "tickets": [
        {
          "assigneeId": {},
          "createdAt": "string",
          "id": "string",
          "name": "Ava Chen",
          "requesterId": "string",
          "requesterWorkspaceId": "string",
          "status": "string",
          "updatedAt": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.page` | number |  |
| `pagination.pageSize` | number |  |
| `pagination.totalCount` | number |  |
| `pagination.totalPages` | number |  |
| `success` | boolean |  |
| `tickets[].assigneeId` | object |  |
| `tickets[].createdAt` | string |  |
| `tickets[].id` | string |  |
| `tickets[].name` | string |  |
| `tickets[].requesterId` | string |  |
| `tickets[].requesterWorkspaceId` | string |  |
| `tickets[].status` | string |  |
| `tickets[].updatedAt` | string |  |

## Native endpoint

Through the native Wrangle API, this operation is `GET /inboxes/:inboxId/tickets` (base URL `https://slack.wrangle.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tickets.md) for the provider-specific parameters and requirements.

