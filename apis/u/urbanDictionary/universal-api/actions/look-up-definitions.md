# Urban Dictionary: Look Up Definitions



```
GET https://connect.mindcloud.co/v1/universal/urbanDictionary/latest/actions/look-up-definitions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Urban Dictionary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/urbanDictionary/latest/actions/look-up-definitions?connectionId=$CONNECTION_ID&term=e.g.%2C%20yeet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "term": "e.g., yeet"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/urbanDictionary/latest/actions/look-up-definitions?${params}`, {
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
| `term` | string | yes | Word or phrase to look up. Example: `e.g., yeet`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "current_vote": "string",
      "defid": 1,
      "definition": "string",
      "example": "string",
      "permalink": "https://example.com",
      "sound_urls": [
        "https://example.com"
      ],
      "thumbs_down": 1,
      "thumbs_up": 1,
      "word": "string",
      "written_on": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string | Definition author. |
| `current_vote` | string | Current vote state. |
| `defid` | number | Definition identifier. |
| `definition` | string | Community-submitted definition text. |
| `example` | string | Community-submitted usage example. |
| `permalink` | string | URL for the definition. |
| `sound_urls` | array<string> | Associated sound URLs when available. |
| `thumbs_down` | number | Negative vote count. |
| `thumbs_up` | number | Positive vote count. |
| `word` | string | Defined word or phrase. |
| `written_on` | date | Definition submission timestamp. |

## Native endpoint

Through the native Urban Dictionary API, this operation is `GET /v0/define` (base URL `https://api.urbandictionary.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/look-up-definitions.md) for the provider-specific parameters and requirements.

