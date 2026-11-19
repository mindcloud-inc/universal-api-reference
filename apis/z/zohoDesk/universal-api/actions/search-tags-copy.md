# Zoho Desk: List Ticket Tags

This API searches for tags added in your help desk portal

```
GET https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/search-tags-copy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Desk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/search-tags-copy?connectionId=$CONNECTION_ID&limit=25&offset=0&departmentID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "departmentID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/search-tags-copy?${params}`, {
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
| `departmentID` | string | yes | ID of the department from which the tags must be fetched. |
| `sortBy` | string | no | Key that sorts tags by a specific attribute: `createdTime` or `count`. The default sorting order is descending. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho Desk API returns.

## Native endpoint

Through the native Zoho Desk API, this operation is `GET /ticketTags` (base URL `https://desk.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-tags-copy.md) for the provider-specific parameters and requirements.

