# Centers for Disease Control and Prevention: Search Media

Finds media in CDC Content Services.

```
GET https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/search-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centers for Disease Control and Prevention `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/search-media?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/search-media?${params}`, {
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
| `audience` | string | no | Filter media by audience. |
| `languageName` | string | no | Comma-separated language names. |
| `mediaTypes` | string | no | Comma-separated media type names. |
| `nameContains` | string | no | Return media whose name contains this text. |
| `q` | string | no | Searches topic, name, and description. |
| `sourceAcronym` | string | no | Filter media by source acronym, such as CDC. |
| `topic` | string | no | Filter media by topic name. |
| `topicIds` | string | no | Comma-separated sub-topic IDs. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Comma-separated first-level fields to return. Defaults to a compact useful media summary. Default: `id,name,description,mediaType,language,source,sourceUrl,targetUrl,datePublished,dateModified,thumbnailUrl`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateModified": "2026-05-07T12:00:00.000Z",
      "datePublished": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "language": {},
      "mediaType": "string",
      "name": "Ava Chen",
      "source": {},
      "sourceUrl": "https://example.com",
      "tags": [
        {}
      ],
      "targetUrl": "https://example.com",
      "thumbnailUrl": "https://example.com",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateModified` | date |  |
| `datePublished` | date |  |
| `description` | string |  |
| `id` | number |  |
| `language` | object |  |
| `mediaType` | string |  |
| `name` | string |  |
| `source` | object |  |
| `sourceUrl` | string |  |
| `tags` | array<object> |  |
| `targetUrl` | string |  |
| `thumbnailUrl` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Centers for Disease Control and Prevention API, this operation is `GET /v2/resources/media` (base URL `https://tools.cdc.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-media.md) for the provider-specific parameters and requirements.

