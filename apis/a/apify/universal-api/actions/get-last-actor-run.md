# Apify: Get Last Actor Run

Retrieves the last run for an Apify actor.

```
GET https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-last-actor-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-last-actor-run?connectionId=$CONNECTION_ID&actorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-last-actor-run?${params}`, {
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
| `actorId` | string | yes | The ID or username of the actor whose latest run to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Apify API returns.

## Native endpoint

Through the native Apify API, this operation is `GET /v2/acts/:actorId/runs/last` (base URL `https://api.apify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-last-actor-run.md) for the provider-specific parameters and requirements.

