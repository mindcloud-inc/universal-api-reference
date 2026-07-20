# Doppler Marketing Automation: List Unsubscribed Subscribers

Retrieves unsubscribed subscribers from Doppler Marketing Automation.

```
GET https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/list-unsubscribed-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doppler Marketing Automation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/list-unsubscribed-subscribers?connectionId=$CONNECTION_ID&from=2015-05-21T09%3A00%3A36-03%3A00&to=2015-01-29T09%3A00%3A36Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "2015-05-21T09:00:36-03:00",
  "to": "2015-01-29T09:00:36Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/list-unsubscribed-subscribers?${params}`, {
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
| `from` | date | yes | Inclusive start date-time filter. Doppler returns a gateway error without a date window. Example: `2015-05-21T09:00:36-03:00`. |
| `to` | date | yes | Exclusive end date-time filter. Doppler returns a gateway error without a date window. Example: `2015-01-29T09:00:36Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": [
        {}
      ],
      "currentPage": 1,
      "items": [
        {}
      ],
      "itemsCount": 1,
      "pagesCount": 1,
      "pageSize": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | array<object> |  |
| `currentPage` | number |  |
| `items` | array<object> |  |
| `itemsCount` | number |  |
| `pagesCount` | number |  |
| `pageSize` | number |  |

## Native endpoint

Through the native Doppler Marketing Automation API, this operation is `GET /accounts/:accountName/unsubscribed` (base URL `https://restapi.fromdoppler.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-unsubscribed-subscribers.md) for the provider-specific parameters and requirements.

