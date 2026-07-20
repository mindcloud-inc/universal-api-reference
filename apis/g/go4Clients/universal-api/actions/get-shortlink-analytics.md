# Go4Clients: Get Shortlink Analytics

Retrieves shortlink campaign analytics from Go4Clients.

```
GET https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/get-shortlink-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/get-shortlink-analytics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/get-shortlink-analytics?${params}`, {
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
| `uniqueCampaignID` | string | no | Campaign ID to filter analytics for one shortlink campaign. Example: `69dd271fcc9a80000773ba02`. |
| `start` | number | no | Initial pagination offset. Example: `0`. |
| `limit` | number | no | Page size, maximum 5000. Example: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
        {}
      ],
      "number": 1,
      "numberOfElements": 1,
      "size": 1,
      "totalElements": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | array<object> | Shortlink analytics rows for the requested campaign. |
| `number` | number | Current page number. |
| `numberOfElements` | number | Number of elements in the current page. |
| `size` | number | Requested page size. |
| `totalElements` | number | Total analytics records returned by the query. |
| `totalPages` | number | Total number of pages in the analytics response. |

## Native endpoint

Through the native Go4Clients API, this operation is `GET /api/analytics/shortlink/v1.0` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shortlink-analytics.md) for the provider-specific parameters and requirements.

