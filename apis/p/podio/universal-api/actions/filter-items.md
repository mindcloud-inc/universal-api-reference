# Podio: Filter Items

Finds items in Podio using filters.

```
GET https://connect.mindcloud.co/v1/universal/podio/latest/actions/filter-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podio/latest/actions/filter-items?connectionId=$CONNECTION_ID&appId=123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "123456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podio/latest/actions/filter-items?${params}`, {
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
| `appId` | number | yes | The app ID. Example: `123456`. |
| `filters` | object | no | The filters object to apply. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sortBy` | string | no | The sort order to use. |
| `sortDesc` | boolean | no | True to sort descending, false otherwise. |
| `limit` | number | no | The maximum number of items to return. Example: `30`. |
| `offset` | number | no | The offset into the returned items. Example: `0`. |
| `remember` | boolean | no | True if the view should be remembered, false otherwise. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filtered": 1,
      "items": [
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
| `filtered` | number | Number of items matching the filter. |
| `items` | array<object> | Returned Podio items. |
| `total` | number | Total number of items in the app. |

## Native endpoint

Through the native Podio API, this operation is `POST /item/app/:app_id/filter/` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/filter-items.md) for the provider-specific parameters and requirements.

