# Nightfall.ai: Get Violation Activity

Retrieves activity for a violation from Nightfall.ai.

```
GET https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/get-violation-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nightfall.ai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/get-violation-activity?connectionId=$CONNECTION_ID&limit=25&offset=0&violationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "violationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/get-violation-activity?${params}`, {
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
| `violationId` | string | yes | The UUID of the violation whose activity you want to fetch. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nightfall.ai API returns.

## Native endpoint

Through the native Nightfall.ai API, this operation is `GET /dlp/v1/violations/:violationId/activity` (base URL `https://api.nightfall.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-violation-activity.md) for the provider-specific parameters and requirements.

