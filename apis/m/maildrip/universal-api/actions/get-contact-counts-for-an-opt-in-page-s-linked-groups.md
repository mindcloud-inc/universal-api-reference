# Maildrip: Get contact counts for an opt-in page's linked groups



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-contact-counts-for-an-opt-in-page-s-linked-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-contact-counts-for-an-opt-in-page-s-linked-groups?connectionId=$CONNECTION_ID&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-contact-counts-for-an-opt-in-page-s-linked-groups?${params}`, {
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
| `pageId` | string | yes | ID of the opt-in page |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactsInGroups": 1,
      "conversionRate": 1,
      "last30Days": 1,
      "last30DaysViews": 1,
      "last7Days": 1,
      "last7DaysViews": 1,
      "lastSignupAt": "2026-05-07T12:00:00.000Z",
      "totalSignups": 1,
      "totalViews": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactsInGroups` | number | Total contacts currently in the linked groups (all acquisition channels) |
| `conversionRate` | number | Percentage of views that resulted in a signup (0–100). Null if no views recorded yet. Note: numerator is contacts in linked groups, which may include contacts added through other channels. Use as an approximation. |
| `last30Days` | number | Contacts added to linked groups in the last 30 days |
| `last30DaysViews` | number | Page views in the last 30 days |
| `last7Days` | number | Contacts added to linked groups in the last 7 days |
| `last7DaysViews` | number | Page views in the last 7 days |
| `lastSignupAt` | date | Timestamp of the most recently added contact in the linked groups |
| `totalSignups` | number | Alias for contactsInGroups — total contacts added via this opt-in page's linked groups |
| `totalViews` | number | Total number of times the public page has been loaded (recorded since this feature was deployed) |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/opt-in-pages/{pageId}/stats` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-counts-for-an-opt-in-page-s-linked-groups.md) for the provider-specific parameters and requirements.

