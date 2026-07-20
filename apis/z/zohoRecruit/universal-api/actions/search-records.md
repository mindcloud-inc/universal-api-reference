# Zoho Recruit: Search Records

Finds records in Zoho Recruit by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/search-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Recruit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/search-records?connectionId=$CONNECTION_ID&limit=25&offset=0&moduleApiName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "moduleApiName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/search-records?${params}`, {
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
| `moduleApiName` | string | yes | The Zoho Recruit module API name to search. |
| `criteria` | string | no | Criteria expression to search records by field values. |
| `email` | string | no | Search records by email across the module email fields. |
| `phone` | string | no | Search records by phone number across the module phone fields. |
| `word` | string | no | Search records globally by a word match. |
| `page` | number | no | Page number of search results to fetch. |
| `perPage` | number | no | Maximum number of search results to fetch per page. |
| `converted` | string | no | Whether to fetch converted, non-converted, or all converted states. One of: `both`, `false`, `true`. |
| `approved` | string | no | Whether to fetch approved, unapproved, or all approval states. One of: `both`, `false`, `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho Recruit API returns.

## Native endpoint

Through the native Zoho Recruit API, this operation is `GET /:moduleApiName/search` (base URL `https://recruit.zoho.com/recruit/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-records.md) for the provider-specific parameters and requirements.

