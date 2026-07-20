# Cloze: Search Companies

Finds companies in Cloze.

```
GET https://connect.mindcloud.co/v1/universal/cloze/latest/actions/search-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/search-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloze/latest/actions/search-companies?${params}`, {
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
| `assigned` | boolean | no | Filter by whether the company is assigned. |
| `assignee` | string | no | Filter by assignee email when assigned is true. |
| `countonly` | boolean | no | Return only the available count without company records. |
| `freeformquery` | string | no | Natural-language or UI-style Cloze query expression. |
| `group` | list<string> | no | Group order for matching companies. One of: `stage`, `subteam`. |
| `pagenumber` | number | no | Page number to retrieve, starting from 1. |
| `pagesize` | number | no | Limit results per page. Default 10, maximum 1000. |
| `scope` | string | no | Scope of matching relations, such as local or team. Set on the initial request. |
| `segment` | string | no | Filter by segment id or current segment name. |
| `sort` | list<string> | no | Sort order for matching companies. One of: `assigned`, `bestrelationship`, `created`, `distance`, `duenext`, `duepast`, `end`, `first`, `firstmet`, `last`, `lastchanged`, `lasttalked`, `name`, `nextstep`, `start`, `value`, `wentquiet`. |
| `stage` | list<string> | no | Filter by company stage. One of: `current`, `future`, `lead`, `out`, `past`. |
| `step` | string | no | Filter by next step unique id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availablecount": 1,
      "companies": [
        [
          {}
        ]
      ],
      "errorcode": 1,
      "pagenumber": 1,
      "pagesize": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availablecount` | number | Count of matching records |
| `companies[]` | array<object> | Array of company records |
| `companies[].assignee` | string | Assignee email |
| `companies[].description` | string | Company description |
| `companies[].direct` | string | Direct identifier |
| `companies[].name` | string | Company name |
| `companies[].segment` | string | Segment |
| `companies[].stage` | string | Stage |
| `errorcode` | number | Error code. 0 means success |
| `pagenumber` | number | Returned page number |
| `pagesize` | number | Returned page size |

## Native endpoint

Through the native Cloze API, this operation is `GET /v1/companies/find` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-companies.md) for the provider-specific parameters and requirements.

