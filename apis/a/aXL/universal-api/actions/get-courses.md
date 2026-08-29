# AXL: Get Courses



```
GET https://connect.mindcloud.co/v1/universal/aXL/latest/actions/get-courses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AXL `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aXL/latest/actions/get-courses?connectionId=$CONNECTION_ID&limit=25&offset=0&fields=%7Bid%2Cname%2CisPublished%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "fields": "{id,name,isPublished}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aXL/latest/actions/get-courses?${params}`, {
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
| `fields` | string | yes | Fields to return using AXL field-selection syntax, for example {id,name,isPublished} Default: `{id,name,shortDescription,isPublished,freeAccess,createdDate,updatedDate,studentCount}`. Example: `{id,name,isPublished}`. |
| `search` | string | no | Search phrase for matching courses Example: `Course name or phrase`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AXL API returns.

## Native endpoint

Through the native AXL API, this operation is `GET /course` (base URL `https://app.axl.tech/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-courses.md) for the provider-specific parameters and requirements.

