# DMSales: List Contact Events

Retrieves contact events from DMSales.

```
GET https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/list-contact-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMSales `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/list-contact-events?connectionId=$CONNECTION_ID&baseKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "baseKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/list-contact-events?${params}`, {
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
| `baseKey` | string | yes | Contact base key. |
| `dateFrom` | date | no | Start date for event filtering (YYYY-MM-DD). |
| `dateTo` | date | no | End date for event filtering (YYYY-MM-DD). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native DMSales API, this operation is `GET /api/contact-card/events` (base URL `https://app.dmsales.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-events.md) for the provider-specific parameters and requirements.

