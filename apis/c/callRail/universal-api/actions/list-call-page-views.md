# CallRail: List Call Page Views

Retrieves page views for a CallRail call.

```
GET https://connect.mindcloud.co/v1/universal/callRail/latest/actions/list-call-page-views
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallRail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callRail/latest/actions/list-call-page-views?connectionId=$CONNECTION_ID&account_id=string&call_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "account_id": "string",
  "call_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callRail/latest/actions/list-call-page-views?${params}`, {
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
| `account_id` | string | yes | The CallRail account ID. |
| `call_id` | string | yes | The CallRail call ID. |
| `time_zone` | string | no | Optional IANA time zone override for page view timestamps. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "page": 1,
      "pageViews": [
        "string"
      ],
      "perPage": 1,
      "totalPages": 1,
      "totalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page` | number |  |
| `pageViews` | array<string> |  |
| `perPage` | number |  |
| `totalPages` | number |  |
| `totalRecords` | number |  |

## Native endpoint

Through the native CallRail API, this operation is `GET /v3/a/:account_id/calls/:call_id/page_views.json` (base URL `https://api.callrail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-call-page-views.md) for the provider-specific parameters and requirements.

