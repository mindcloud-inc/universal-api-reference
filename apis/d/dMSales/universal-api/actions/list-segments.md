# DMSales: List Segments

Retrieves segments from DMSales.

```
GET https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/list-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMSales `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/list-segments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/list-segments?${params}`, {
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
| `withFilters` | boolean | no | Whether to include segment filters. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "id": "string",
      "main": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `id` | string |  |
| `main` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native DMSales API, this operation is `GET /api/segment/list` (base URL `https://app.dmsales.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-segments.md) for the provider-specific parameters and requirements.

