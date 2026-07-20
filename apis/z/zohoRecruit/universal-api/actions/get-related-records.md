# Zoho Recruit: Get Related Records

Retrieves related records from Zoho Recruit.

```
GET https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/get-related-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Recruit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/get-related-records?connectionId=$CONNECTION_ID&limit=25&offset=0&moduleApiName=Ava%20Chen&recordId=string&relatedModule=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "moduleApiName": "Ava Chen",
  "recordId": "string",
  "relatedModule": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/get-related-records?${params}`, {
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
| `moduleApiName` | string | yes | The Zoho Recruit module API name that owns the related records. |
| `recordId` | string | yes | The unique ID of the base Zoho Recruit record. |
| `relatedModule` | string | yes | The related list API name, such as Attachments or Notes. |
| `ids` | string | no | Comma-separated related record IDs to filter the related-record response. Accepts multiple values in one string, delimited by `,`. |
| `fields` | string | no | Comma-separated field API names to include in the related-record response. |
| `page` | number | no | Page number of related records to fetch. |
| `perPage` | number | no | Maximum number of related records to fetch per page. |
| `sortBy` | string | no | Field API name to sort the related records by. |
| `sortOrder` | string | no | Sort order to apply to the selected sort field. One of: `asc`, `desc`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho Recruit API returns.

## Native endpoint

Through the native Zoho Recruit API, this operation is `GET /:moduleApiName/:recordId/:relatedModule` (base URL `https://recruit.zoho.com/recruit/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-related-records.md) for the provider-specific parameters and requirements.

