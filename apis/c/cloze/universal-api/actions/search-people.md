# Cloze: Search People

Finds people in Cloze.

```
GET https://connect.mindcloud.co/v1/universal/cloze/latest/actions/search-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/search-people?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloze/latest/actions/search-people?${params}`, {
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
| `assigned` | boolean | no | Filter by whether the person is assigned. |
| `assignee` | string | no | Filter by assignee email when assigned is true. |
| `countonly` | boolean | no | Return only the available count without person records. |
| `freeformquery` | string | no | Natural-language or UI-style Cloze query expression. |
| `group` | list<string> | no | Group order for matching people. One of: `stage`, `subteam`. |
| `pagenumber` | number | no | Page number to retrieve, starting from 1. |
| `pagesize` | number | no | Limit results per page. Default 10, maximum 1000. |
| `scope` | string | no | Scope of matching relations, such as local or team. Set on the initial request. |
| `segment` | string | no | Filter by segment id or current segment name. |
| `sort` | list<string> | no | Sort order for matching people. One of: `assigned`, `bestrelationship`, `created`, `distance`, `duenext`, `duepast`, `end`, `first`, `firstmet`, `last`, `lastchanged`, `lasttalked`, `name`, `nextstep`, `start`, `value`, `wentquiet`. |
| `stage` | list<string> | no | Filter by person stage. One of: `current`, `future`, `lead`, `out`, `past`. |
| `step` | string | no | Filter by next step unique id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availablecount": 1,
      "errorcode": 1,
      "pagenumber": 1,
      "pagesize": 1,
      "people": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availablecount` | number | Count of matching records |
| `errorcode` | number | Error code. 0 means success |
| `pagenumber` | number | Returned page number |
| `pagesize` | number | Returned page size |
| `people[]` | array<object> | Array of person records |
| `people[].assignee` | string | Assignee email |
| `people[].direct` | string | Direct identifier |
| `people[].first` | string | First name |
| `people[].last` | string | Last name |
| `people[].name` | string | Full name |
| `people[].segment` | string | Segment |
| `people[].stage` | string | Stage |

## Native endpoint

Through the native Cloze API, this operation is `GET /v1/people/find` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-people.md) for the provider-specific parameters and requirements.

