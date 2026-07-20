# AMcards.com: List Quicksend Templates

Retrieves Quicksend templates from your AMcards.com account.

```
GET https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/list-quicksend-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AMcards.com `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/list-quicksend-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/list-quicksend-templates?${params}`, {
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
| `nameContains` | string | no | Filter quicksend templates by partial name match. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deprecated": true,
      "envelopeFont": {},
      "envelopeSpecialMessage": {},
      "hasMessageOnDefaultPanel": "string",
      "id": 1,
      "isBlast": true,
      "lastModified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "nameWithGifts": "Ava Chen",
      "resourceUri": "string",
      "thumbnail": "string",
      "thumbnailUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deprecated` | boolean |  |
| `envelopeFont` | object |  |
| `envelopeSpecialMessage` | object |  |
| `hasMessageOnDefaultPanel` | string |  |
| `id` | number |  |
| `isBlast` | boolean |  |
| `lastModified` | date |  |
| `name` | string |  |
| `nameWithGifts` | string |  |
| `resourceUri` | string |  |
| `thumbnail` | string |  |
| `thumbnailUrl` | string |  |

## Native endpoint

Through the native AMcards.com API, this operation is `GET /quicksendtemplate/` (base URL `https://amcards.com/.api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-quicksend-templates.md) for the provider-specific parameters and requirements.

