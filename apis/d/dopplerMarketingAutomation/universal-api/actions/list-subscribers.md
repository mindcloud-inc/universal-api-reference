# Doppler Marketing Automation: List Subscribers

Retrieves subscribers from a Doppler Marketing Automation list.

```
GET https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/list-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doppler Marketing Automation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/list-subscribers?connectionId=$CONNECTION_ID&listId=509702" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "509702"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/list-subscribers?${params}`, {
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
| `listId` | string | yes | Doppler list identifier. Example: `509702`. |

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

Through the native Doppler Marketing Automation API, this operation is `GET /accounts/:accountName/lists/:listId/subscribers` (base URL `https://restapi.fromdoppler.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscribers.md) for the provider-specific parameters and requirements.

