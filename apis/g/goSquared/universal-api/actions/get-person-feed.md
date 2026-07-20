# GoSquared: Get Person Feed

Retrieves a person's feed events from GoSquared.

```
GET https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/get-person-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoSquared `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/get-person-feed?connectionId=$CONNECTION_ID&limit=25&offset=0&personId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "personId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/get-person-feed?${params}`, {
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
| `personId` | string | yes | The unique identifier of the person whose feed should be retrieved. |
| `query` | string | no | The query term used to search through the person's event history. |
| `type` | string | no | Comma-delimited event types to include in the feed. Default: `event,sessionEvent`. |
| `from` | string | no | The start date-time for the feed query. |
| `to` | string | no | The end date-time for the feed query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "id": "string",
      "name": "Ava Chen",
      "timestamp": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Provider-specific event payload details. |
| `id` | string | GoSquared event identifier. |
| `name` | string | Display name for the feed event. |
| `timestamp` | string | Timestamp for the feed event. |
| `type` | string | Event type reported in the person's feed. |

## Native endpoint

Through the native GoSquared API, this operation is `GET people/v1/people/:personID/feed` (base URL `https://api.gosquared.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-person-feed.md) for the provider-specific parameters and requirements.

