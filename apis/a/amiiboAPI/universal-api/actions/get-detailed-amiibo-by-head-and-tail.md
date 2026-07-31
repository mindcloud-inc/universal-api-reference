# Amiibo API: Get Detailed Amiibo by Head and Tail



```
GET https://connect.mindcloud.co/v1/universal/amiiboAPI/latest/actions/get-detailed-amiibo-by-head-and-tail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amiibo API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amiiboAPI/latest/actions/get-detailed-amiibo-by-head-and-tail?connectionId=$CONNECTION_ID&head=string&tail=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "head": "string",
  "tail": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amiiboAPI/latest/actions/get-detailed-amiibo-by-head-and-tail?${params}`, {
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
| `head` | string | yes | Required 8-digit hexadecimal head identifier. |
| `tail` | string | yes | Required 8-digit hexadecimal tail identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amiibo": [
        {
          "amiiboSeries": "string",
          "character": "string",
          "games3DS": [
            {}
          ],
          "gameSeries": "string",
          "gamesSwitch": [
            {}
          ],
          "gamesWiiU": [
            {}
          ],
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amiibo` | array<object> | Native AmiiboAPI result envelope. |
| `amiibo[].amiiboSeries` | string | Amiibo series. |
| `amiibo[].character` | string | Character. |
| `amiibo[].games3DS` | array<object> | Nintendo 3DS game-usage records. |
| `amiibo[].gameSeries` | string | Game series. |
| `amiibo[].gamesSwitch` | array<object> | Nintendo Switch game-usage records. |
| `amiibo[].gamesWiiU` | array<object> | Wii U game-usage records. |
| `amiibo[].head` | string | 8-digit hexadecimal head identifier. |
| `amiibo[].image` | string | Provider image URL. |
| `amiibo[].name` | string | Amiibo name. |
| `amiibo[].release.au` | date | Australia release date, if known. |
| `amiibo[].release.eu` | date | Europe release date, if known. |
| `amiibo[].release.jp` | date | Japan release date, if known. |
| `amiibo[].release.na` | date | North America release date, if known. |
| `amiibo[].tail` | string | 8-digit hexadecimal tail identifier. |
| `amiibo[].type` | string | Amiibo type. |

## Native endpoint

Through the native Amiibo API API, this operation is `GET /api/amiibofull/` (base URL `https://amiiboapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-detailed-amiibo-by-head-and-tail.md) for the provider-specific parameters and requirements.

