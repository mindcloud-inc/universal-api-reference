# ShinyStat: Get Time On Site

Retrieves time on site metrics from ShinyStat.

```
GET https://connect.mindcloud.co/v1/universal/shinyStat/latest/actions/get-time-on-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShinyStat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shinyStat/latest/actions/get-time-on-site?connectionId=$CONNECTION_ID&href=%2F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "href": "/"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shinyStat/latest/actions/get-time-on-site?${params}`, {
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
| `href` | string | yes | Temporary default route for this report. Replace with the exact internal ShinyStat report route once authenticated dashboard evidence is available. Default: `/`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ShinyStat API returns.

## Native endpoint

Through the native ShinyStat API, this operation is `POST /ajax` (base URL `https://report.shinystat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-on-site.md) for the provider-specific parameters and requirements.

