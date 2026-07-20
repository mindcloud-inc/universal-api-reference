# Recombee: List Series Items

Retrieves items from a Recombee series.

```
GET https://connect.mindcloud.co/v1/universal/recombee/latest/actions/list-series-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recombee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recombee/latest/actions/list-series-items?connectionId=$CONNECTION_ID&seriesId=series-123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "seriesId": "series-123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recombee/latest/actions/list-series-items?${params}`, {
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
| `seriesId` | string | yes | Example: `series-123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "itemId": "string",
      "itemType": "string",
      "time": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `itemId` | string | Item ID contained in the series. |
| `itemType` | string | Type of series entry returned by Recombee. |
| `time` | number | Numeric ordering value stored for the series item. |

## Native endpoint

Through the native Recombee API, this operation is `GET /series/:seriesId/items/` (base URL `https://rapi.recombee.com/{{credentials.databaseId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-series-items.md) for the provider-specific parameters and requirements.

