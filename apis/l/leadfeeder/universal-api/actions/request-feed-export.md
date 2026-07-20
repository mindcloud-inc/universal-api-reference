# Leadfeeder: Request Feed Export

Creates a custom feed export request in Leadfeeder.

```
POST https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/request-feed-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadfeeder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/request-feed-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customFeedId": "all_leads",
  "startDate": "2026-04-01",
  "endDate": "2026-04-13"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/request-feed-export', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customFeedId": "all_leads",
    "startDate": "2026-04-01",
    "endDate": "2026-04-13"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customFeedId` | string | yes | Example: `all_leads`. |
| `startDate` | date | yes | Example: `2026-04-01`. |
| `endDate` | date | yes | Example: `2026-04-13`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadfeeder API returns.

## Native endpoint

Through the native Leadfeeder API, this operation is `POST /export-requests` (base URL `https://api.leadfeeder.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-feed-export.md) for the provider-specific parameters and requirements.

