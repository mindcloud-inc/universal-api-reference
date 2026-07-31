# Amiibo API: Get Game Series by Key



```
GET https://connect.mindcloud.co/v1/universal/amiiboAPI/latest/actions/get-game-series-by-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amiibo API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amiiboAPI/latest/actions/get-game-series-by-key?connectionId=$CONNECTION_ID&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amiiboAPI/latest/actions/get-game-series-by-key?${params}`, {
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
| `key` | string | yes | Required 3-digit hexadecimal game-series key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amiibo": {
        "key": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amiibo` | object | Native AmiiboAPI metadata envelope. |
| `amiibo.key` | string | Hexadecimal metadata key. |
| `amiibo.name` | string | Metadata name. |

## Native endpoint

Through the native Amiibo API API, this operation is `GET /api/gameseries/` (base URL `https://amiiboapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-game-series-by-key.md) for the provider-specific parameters and requirements.

