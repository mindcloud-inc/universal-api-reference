# Centers for Disease Control and Prevention: List Tags

Retrieves tags from CDC Content Services.

```
GET https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centers for Disease Control and Prevention `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/list-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/list-tags?${params}`, {
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
| `language` | string | no | Filter tags by language. |
| `nameContains` | string | no | Return tags whose names contain this text. |
| `typeName` | string | no | Return tags belonging to this tag type name. |
| `mediaId` | number | no | Return tags associated with this media ID. |
| `typeId` | number | no | Return tags belonging to this tag type ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "language": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `language` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centers for Disease Control and Prevention API, this operation is `GET /v2/resources/tags` (base URL `https://tools.cdc.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

