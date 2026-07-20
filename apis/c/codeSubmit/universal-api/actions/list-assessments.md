# CodeSubmit: List Assessments



```
GET https://connect.mindcloud.co/v1/universal/codeSubmit/latest/actions/list-assessments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeSubmit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeSubmit/latest/actions/list-assessments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeSubmit/latest/actions/list-assessments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
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
| `count` | number | Total assessments returned by this query. |
| `next` | string | Pagination cursor or URL for the next page, when present. |
| `previous` | string | Pagination cursor or URL for the previous page, when present. |
| `results` | array<object> | Assessment result rows. |

## Native endpoint

Through the native CodeSubmit API, this operation is `GET /api/external/tests` (base URL `https://app.codesubmit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-assessments.md) for the provider-specific parameters and requirements.

