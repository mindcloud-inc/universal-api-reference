# 3Scribe: List Transcription Jobs

Retrieves transcription jobs from your 3Scribe account.

```
GET https://connect.mindcloud.co/v1/universal/scribe/latest/actions/list-transcription-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 3Scribe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scribe/latest/actions/list-transcription-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scribe/latest/actions/list-transcription-jobs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 3Scribe API returns.

## Native endpoint

Through the native 3Scribe API, this operation is `GET /jobs` (base URL `https://api.3scri.be`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transcription-jobs.md) for the provider-specific parameters and requirements.

