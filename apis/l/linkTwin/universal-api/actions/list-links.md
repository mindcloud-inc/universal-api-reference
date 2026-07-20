# LinkTwin: List Links

Retrieves your shortened links from LinkTwin.

```
GET https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/list-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkTwin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/list-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/list-links?${params}`, {
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
| `limit` | number | no | Per page data result. |
| `page` | number | no | Current page request. |
| `order` | string | no | Sort order. |
| `search` | string | no | Search links. |
| `dateFrom` | string | no | Start date filter. |
| `dateTo` | string | no | End date filter. |
| `collections` | string | no | JSON array string of collection IDs or names. |
| `timezone` | string | no | Timezone override for response dates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentpage": 1,
      "maxpage": 1,
      "nextpage": {},
      "perpage": 1,
      "result": 1,
      "usage": {
        "clicks": 1,
        "clicksLimit": 1,
        "clicksResetDays": 1,
        "missedClicks": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentpage` | number |  |
| `maxpage` | number |  |
| `nextpage` | object |  |
| `perpage` | number |  |
| `result` | number |  |
| `usage.clicks` | number |  |
| `usage.clicksLimit` | number |  |
| `usage.clicksResetDays` | number |  |
| `usage.missedClicks` | number |  |

## Native endpoint

Through the native LinkTwin API, this operation is `GET /urls` (base URL `https://linktw.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-links.md) for the provider-specific parameters and requirements.

