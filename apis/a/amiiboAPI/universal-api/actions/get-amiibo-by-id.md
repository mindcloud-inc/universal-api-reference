# Amiibo API: Get Amiibo by ID



```
GET https://connect.mindcloud.co/v1/universal/amiiboAPI/latest/actions/get-amiibo-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amiibo API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amiiboAPI/latest/actions/get-amiibo-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amiiboAPI/latest/actions/get-amiibo-by-id?${params}`, {
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
| `id` | string | yes | Required 16-digit hexadecimal Amiibo ID, optionally 0x-prefixed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amiibo": {
        "amiiboSeries": "string",
        "character": "string",
        "gameSeries": "string",
        "head": "string",
        "image": "string",
        "name": "Ava Chen",
        "release": {
          "au": "2026-05-07T12:00:00.000Z",
          "eu": "2026-05-07T12:00:00.000Z",
          "jp": "2026-05-07T12:00:00.000Z",
          "na": "2026-05-07T12:00:00.000Z"
        },
        "tail": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amiibo` | object | Native AmiiboAPI result envelope. |
| `amiibo.amiiboSeries` | string | Amiibo series. |
| `amiibo.character` | string | Character. |
| `amiibo.gameSeries` | string | Game series. |
| `amiibo.head` | string | 8-digit hexadecimal head identifier. |
| `amiibo.image` | string | Provider image URL. |
| `amiibo.name` | string | Amiibo name. |
| `amiibo.release.au` | date | Australia release date, if known. |
| `amiibo.release.eu` | date | Europe release date, if known. |
| `amiibo.release.jp` | date | Japan release date, if known. |
| `amiibo.release.na` | date | North America release date, if known. |
| `amiibo.tail` | string | 8-digit hexadecimal tail identifier. |
| `amiibo.type` | string | Amiibo type. |

## Native endpoint

Through the native Amiibo API API, this operation is `GET /api/amiibo/` (base URL `https://amiiboapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-amiibo-by-id.md) for the provider-specific parameters and requirements.

