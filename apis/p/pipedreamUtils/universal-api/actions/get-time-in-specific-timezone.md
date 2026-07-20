# Pipedream Utils: Helper Functions - Get Time in Timezone

Converts an ISO timestamp to a timezone in Pipedream Utils.

```
GET https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/get-time-in-specific-timezone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream Utils `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/get-time-in-specific-timezone?connectionId=$CONNECTION_ID&time=string&timezone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "time": "string",
  "timezone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/get-time-in-specific-timezone?${params}`, {
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
| `time` | string | yes | An [ISO 8601 string](https://en.wikipedia.org/wiki/ISO_8601) representing the time you'd like to convert to your target timezone. If this timestamp doesn't have a timezone component, it's assumed to be in UTC. |
| `timezone` | string | yes | The IANA timezone name, e.g. `America/Los_Angeles`. [See the full list here](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pipedream Utils API returns.

## Native endpoint

Through the native Pipedream Utils API, this operation is `GET` (base URL `https://pipedream.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-in-specific-timezone.md) for the provider-specific parameters and requirements.

