# NewsData.io: Count Archived News



```
GET https://connect.mindcloud.co/v1/universal/newsDataio/latest/actions/count-archived-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsData.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsDataio/latest/actions/count-archived-news?connectionId=$CONNECTION_ID&fromDate=2026-04-20&toDate=2026-04-21" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromDate": "2026-04-20",
  "toDate": "2026-04-21"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsDataio/latest/actions/count-archived-news?${params}`, {
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
| `fromDate` | string | yes | Start date for archive count calculation. Use `YYYY-MM-DD` or `YYYY-MM-DD HH:MM:SS`. Example: `2026-04-20`. |
| `interval` | string | no | Grouping interval for count results. |
| `q` | string | no | Keyword or phrase used for archive count estimation. |
| `toDate` | string | yes | End date for archive count calculation. Use `YYYY-MM-DD` or `YYYY-MM-DD HH:MM:SS`. Example: `2026-04-21`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> | Returned count rows. |
| `status` | string | Request status. |

## Native endpoint

Through the native NewsData.io API, this operation is `GET /count` (base URL `https://newsdata.io/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-archived-news.md) for the provider-specific parameters and requirements.

