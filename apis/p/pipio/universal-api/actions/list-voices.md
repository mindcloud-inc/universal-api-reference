# Pipio: List Voices

Finds available voice options in Pipio.

```
GET https://connect.mindcloud.co/v1/universal/pipio/latest/actions/list-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipio/latest/actions/list-voices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipio/latest/actions/list-voices?${params}`, {
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
| `languages` | string | no | Filter voices by language code. Default: `en-US`. Example: `en-US`. |
| `gender` | list | no | Filter voices by gender. One of: `female`, `male`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `voiceTypes` | list | no | Filter voices by voice type. One of: `Character`, `Conversational`, `Narration`, `Promotional`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "more": true,
      "page": 1,
      "pageSize": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> | Voice records for the current page. |
| `more` | boolean | Whether another page exists. |
| `page` | number | Current page number. |
| `pageSize` | number | Items requested per page. |
| `total` | number | Total matching voices. |

## Native endpoint

Through the native Pipio API, this operation is `GET /voice` (base URL `https://avatar.pipio.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-voices.md) for the provider-specific parameters and requirements.

