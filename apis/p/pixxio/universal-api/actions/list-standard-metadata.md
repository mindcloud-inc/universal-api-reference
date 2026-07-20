# pixx.io: List Standard Metadata

Retrieves standard metadata from your pixx.io workspace.

```
GET https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/list-standard-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pixx.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/list-standard-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/list-standard-metadata?${params}`, {
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
| `ids` | number<number> | no | Filter standard metadata by IDs. Accepts multiple values as an array. |
| `searchTerm` | string | no | Search standard metadata fields by term. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "standardMetadata": {
        "id": 1,
        "name": "Ava Chen"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `standardMetadata` | array<object> |  |
| `standardMetadata.id` | number |  |
| `standardMetadata.name` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native pixx.io API, this operation is `GET /metadata/standard` (base URL `https://mindcloudpixx260413.px.media/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-standard-metadata.md) for the provider-specific parameters and requirements.

