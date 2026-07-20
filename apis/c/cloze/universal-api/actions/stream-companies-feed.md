# Cloze: Stream Companies Feed

Retrieves the companies feed from Cloze.

```
GET https://connect.mindcloud.co/v1/universal/cloze/latest/actions/stream-companies-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/stream-companies-feed?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloze/latest/actions/stream-companies-feed?${params}`, {
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
| `cursor` | string | no | Cursor returned by the previous feed response. |
| `freeformquery` | string | no | Natural-language or UI-style Cloze query expression on the initial request. |
| `includeauditedchanges` | boolean | no | Return change audit details in results for each delivered company. |
| `keysonly` | boolean | no | Return only the syncKey field for each record. |
| `modifiedafter` | string | no | UTC milliseconds or now. Set on the initial request to control the feed starting point. |
| `pagesize` | number | no | Limit results per batch. Set on the initial request. |
| `scope` | string | no | Scope of matching relations. Set on the initial request. |
| `segment` | string | no | Filter by segment on the initial request. |
| `stage` | list<string> | no | Filter by stage on the initial request. One of: `current`, `future`, `lead`, `out`, `past`. |

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
      "cursor": "string",
      "errorcode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availablecount` | number | Count of currently available records |
| `companies[]` | array<object> | Array of streamed company records |
| `companies[].assignee` | string | Assignee email |
| `companies[].direct` | string | Direct identifier |
| `companies[].name` | string | Company name |
| `companies[].segment` | string | Segment |
| `companies[].stage` | string | Stage |
| `cursor` | string | Cursor for the next batch |
| `errorcode` | number | Error code. 0 means success |

## Native endpoint

Through the native Cloze API, this operation is `GET /v1/companies/feed` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stream-companies-feed.md) for the provider-specific parameters and requirements.

