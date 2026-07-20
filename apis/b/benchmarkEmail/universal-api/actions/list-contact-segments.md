# Benchmark Email: List Contact Segments

Retrieves contact segments from Benchmark Email.

```
GET https://connect.mindcloud.co/v1/universal/benchmarkEmail/latest/actions/list-contact-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Benchmark Email `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/benchmarkEmail/latest/actions/list-contact-segments?connectionId=$CONNECTION_ID&filter=string&orderBy=Name&pageSize=100&sortOrder=ASC" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filter": "string",
  "orderBy": "Name",
  "pageSize": "100",
  "sortOrder": "ASC"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/benchmarkEmail/latest/actions/list-contact-segments?${params}`, {
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
| `filter` | string | yes | Optional segment name filter. |
| `orderBy` | string | yes | Segment sort column. Default: `Name`. |
| `pageNumber` | string | no | Optional page number for segment results. Default: `1`. |
| `pageSize` | string | yes | Number of segment rows to return. Default: `100`. |
| `sortOrder` | string | yes | Segment sort direction. Default: `ASC`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Benchmark Email API returns.

## Native endpoint

Through the native Benchmark Email API, this operation is `GET /Contact/Segments` (base URL `https://clientapi.benchmarkemail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-segments.md) for the provider-specific parameters and requirements.

