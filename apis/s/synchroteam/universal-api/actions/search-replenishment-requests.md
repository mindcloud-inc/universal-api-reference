# Synchroteam: Search Replenishment Requests

Finds replenishment requests in Synchroteam using supported filters.

```
GET https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/search-replenishment-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Synchroteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/search-replenishment-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/search-replenishment-requests?${params}`, {
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
| `filters` | object | no | Optional. Provide the Synchroteam stock request search filters object (per docs). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "destination": {
        "idStock": 1
      },
      "id": "string",
      "isDeleted": true,
      "isSent": true,
      "isUrgent": true,
      "part": {
        "idPiece": 1,
        "nmPiece": "string"
      },
      "quantity": 1,
      "source": {
        "idStock": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `destination.idStock` | number |  |
| `id` | string |  |
| `isDeleted` | boolean |  |
| `isSent` | boolean |  |
| `isUrgent` | boolean |  |
| `part.idPiece` | number |  |
| `part.nmPiece` | string |  |
| `quantity` | number |  |
| `source.idStock` | number |  |

## Native endpoint

Through the native Synchroteam API, this operation is `POST /Api/v2/StockRequest/Search` (base URL `https://ws.synchroteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-replenishment-requests.md) for the provider-specific parameters and requirements.

