# Pabbly Hook: Filter Events



```
GET https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/filter-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Hook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/filter-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/filter-events?${params}`, {
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
| `requestId` | string | no | Request ID selector. Example: `req_cd5a26f12b4549c59247742e12e9f7ab`. |
| `status` | string | no | Event status selector. Example: `SUCCESSFUL`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "data": [
        {}
      ],
      "page": 1,
      "total": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number | Current page number. |
| `data` | array<object> | Event records returned by Pabbly Hook. |
| `page` | number | Current page number when returned as page. |
| `total` | number | Total matching event records. |
| `totalPages` | number | Total number of pages. |

## Native endpoint

Through the native Pabbly Hook API, this operation is `GET /api/v1/events` (base URL `https://hook.pabbly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/filter-events.md) for the provider-specific parameters and requirements.

