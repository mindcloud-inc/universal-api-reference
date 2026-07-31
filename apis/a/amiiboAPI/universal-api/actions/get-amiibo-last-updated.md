# Amiibo API: Get Amiibo Last Updated



```
GET https://connect.mindcloud.co/v1/universal/amiiboAPI/latest/actions/get-amiibo-last-updated
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amiibo API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amiiboAPI/latest/actions/get-amiibo-last-updated?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amiiboAPI/latest/actions/get-amiibo-last-updated?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "lastUpdated": {
        "amiibo_sha1": "string",
        "game_info_sha1": "string",
        "timestamp": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lastUpdated` | object | Native last-update envelope. |
| `lastUpdated.amiibo_sha1` | string | Archived Amiibo dataset SHA-1. |
| `lastUpdated.game_info_sha1` | string | Archived game-info dataset SHA-1. |
| `lastUpdated.timestamp` | date | Archived source dataset timestamp. |

## Native endpoint

Through the native Amiibo API API, this operation is `GET /api/lastupdated/` (base URL `https://amiiboapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-amiibo-last-updated.md) for the provider-specific parameters and requirements.

