# Mixpanel: Export Events

Retrieves raw events from Mixpanel.

```
GET https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/export-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mixpanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/export-events?connectionId=$CONNECTION_ID&fromDate=string&toDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromDate": "string",
  "toDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/export-events?${params}`, {
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
| `fromDate` | string | yes | Inclusive start date in YYYY-MM-DD format. |
| `toDate` | string | yes | Inclusive end date in YYYY-MM-DD format. |
| `limit` | number | no | Optional maximum number of events to return; cannot exceed 100000. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event` | string | no | Optional JSON-encoded array of event names to export. |
| `where` | string | no | Optional Mixpanel expression used to filter exported events. |
| `projectId` | number | no | Required if using service account authentication for this request. |
| `timeInMs` | boolean | no | Return timestamps in milliseconds when true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Raw line-delimited event export output or termination text returned by Mixpanel. |

## Native endpoint

Through the native Mixpanel API, this operation is `GET https://data.mixpanel.com/api/2.0/export` (base URL `https://mixpanel.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-events.md) for the provider-specific parameters and requirements.

