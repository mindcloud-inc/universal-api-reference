# Loop Returns: Get Happy Returns Shipments



```
GET https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/new-action1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loop Returns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/new-action1?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/new-action1?${params}`, {
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
| `from` | string | no | Example: `2026-10-09T00:00:00Z`. |
| `to` | string | no | Example: `2026-11-08T23:59:59Z`. |
| `page` | number | no | Default: `1`. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "firstPageUrl": "https://example.com",
      "from": {},
      "lastPage": 1,
      "lastPageUrl": "https://example.com",
      "links": [
        {
          "active": true,
          "label": "https://example.com",
          "page": {},
          "url": {}
        }
      ],
      "nextPageUrl": {},
      "path": "string",
      "perPage": 1,
      "prevPageUrl": {},
      "to": {},
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number |  |
| `firstPageUrl` | string |  |
| `from` | object |  |
| `lastPage` | number |  |
| `lastPageUrl` | string |  |
| `links[].active` | boolean |  |
| `links[].label` | string |  |
| `links[].page` | object |  |
| `links[].url` | object |  |
| `nextPageUrl` | object |  |
| `path` | string |  |
| `perPage` | number |  |
| `prevPageUrl` | object |  |
| `to` | object |  |
| `total` | number |  |

## Native endpoint

Through the native Loop Returns API, this operation is `GET /happy-returns/shipments` (base URL `https://api.loopreturns.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/new-action1.md) for the provider-specific parameters and requirements.

