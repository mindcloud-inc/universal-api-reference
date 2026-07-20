# Mifiel: Search Advanced Information

Searches advanced document information in Mifiel.

```
GET https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/search-advanced-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mifiel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/search-advanced-information?connectionId=$CONNECTION_ID&fields=string&resource=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fields": "string",
  "resource": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/search-advanced-information?${params}`, {
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
| `fields` | string | yes | Fields to return when getting results. |
| `resource` | string | yes | Object on which the search will be made. |
| `page` | number | no | Page number to get results. |
| `perPage` | number | no | Number of records to get per page. |
| `q` | object | no | Search object keyed by field name with string or numeric term operators. |
| `sort` | string | no | Sorting method, for example created_at-desc. |
| `version` | string | no | Endpoint version. Latest documented value is 1.0.0. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "___metadata": {
        "page": 1,
        "page_count": 1,
        "per_page": 1,
        "total_count": 1
      },
      "records": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `___metadata` | object | Pagination metadata for the query response |
| `___metadata.page` | number | Current page number |
| `___metadata.page_count` | number | Total number of pages |
| `___metadata.per_page` | number | Number of records per page |
| `___metadata.total_count` | number | Total number of matching records |
| `records` | array<object> | Array of documents matching the query criteria |

## Native endpoint

Through the native Mifiel API, this operation is `POST /api/query` (base URL `https://app.mifiel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-advanced-information.md) for the provider-specific parameters and requirements.

