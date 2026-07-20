# Sertifier: List Attributes

Finds attributes in Sertifier by search filters.

```
GET https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/list-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sertifier `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/list-attributes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/list-attributes?${params}`, {
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
| `searchTerm` | string | no | Filter attributes by title. |
| `types[]` | array<number> | no | Optional attribute type filters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayFormat": "string",
      "id": "string",
      "title": "string",
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayFormat` | string |  |
| `id` | string |  |
| `title` | string |  |
| `type` | number |  |

## Native endpoint

Through the native Sertifier API, this operation is `POST /attribute/search` (base URL `https://b2b.sertifier.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-attributes.md) for the provider-specific parameters and requirements.

