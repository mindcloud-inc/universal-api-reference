# Podio: Filter Items by View

Finds items in a Podio view.

```
GET https://connect.mindcloud.co/v1/universal/podio/latest/actions/filter-items-by-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podio/latest/actions/filter-items-by-view?connectionId=$CONNECTION_ID&appId=123456&viewId=all_by_date" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "123456",
  "viewId": "all_by_date"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podio/latest/actions/filter-items-by-view?${params}`, {
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
| `viewId` | string | yes | The view ID. Example: `all_by_date`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sortBy` | string | no | The sort order to use. If omitted, Podio uses the sort order from the view. |
| `sortDesc` | boolean | no | True to sort descending, false otherwise. If omitted, Podio uses the sort order from the view. |
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
| `filtered` | number |  |
| `items` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native Podio API, this operation is `POST /item/app/:app_id/filter/:view_id/` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/filter-items-by-view.md) for the provider-specific parameters and requirements.

