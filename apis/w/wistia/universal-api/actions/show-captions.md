# Wistia: Show Captions

Retrieves captions for a Wistia media in one language.

```
GET https://connect.mindcloud.co/v1/universal/wistia/latest/actions/show-captions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wistia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wistia/latest/actions/show-captions?connectionId=$CONNECTION_ID&mediaHashedId=string&languageCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaHashedId": "string",
  "languageCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wistia/latest/actions/show-captions?${params}`, {
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
| `mediaHashedId` | string | yes |  |
| `languageCode` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "englishName": "Ava Chen",
      "id": "string",
      "isDraft": true,
      "language": "string",
      "nativeName": "Ava Chen",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursor` | string | A cursor for stable pagination based on current `sort_by` order. You can pass this to `cursor[before]` or `cursor[after]` as a parameter to fetch the records before or after this record in the same sort order. This is only populated if records were fetched with `cursor[enabled]`, or `cursor[before]` or `cursor[after]`. |
| `englishName` | string | English name of the language. |
| `id` | string | The unique hashed identifier of the time-coded transcript. |
| `isDraft` | boolean |  |
| `language` | string | A 3 character language code as specified by ISO-639–2. |
| `nativeName` | string | Native name of the language. |
| `text` | string | The text of the captions for the specified language in SRT format. |

## Native endpoint

Through the native Wistia API, this operation is `GET /modern/medias/:mediaHashedId/captions/:languageCode` (base URL `https://api.wistia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-captions.md) for the provider-specific parameters and requirements.

