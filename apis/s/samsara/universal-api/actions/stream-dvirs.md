# Samsara: Stream DVIRs



```
GET https://connect.mindcloud.co/v1/universal/samsara/latest/actions/stream-dvirs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samsara `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samsara/latest/actions/stream-dvirs?connectionId=$CONNECTION_ID&limit=25&offset=0&startTime=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "startTime": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/samsara/latest/actions/stream-dvirs?${params}`, {
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
| `startTime` | string | yes | DVIR stream start in RFC 3339 format. |
| `endTime` | string | no | DVIR stream end in RFC 3339 format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Samsara API returns.

## Native endpoint

Through the native Samsara API, this operation is `GET dvirs/stream` (base URL `https://api.samsara.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/stream-dvirs.md) for the provider-specific parameters and requirements.

