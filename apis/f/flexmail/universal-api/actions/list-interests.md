# Flexmail: List Interests

Retrieves available contact interests from Flexmail.

```
GET https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/list-interests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexmail `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/list-interests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/list-interests?${params}`, {
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
| `name` | string | no |  |
| `visibility` | string | no |  |
| `orderBy` | string | no |  |
| `orderDirection` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "label": "string",
      "name": "Ava Chen",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | The description of the interest. |
| `id` | string | The identifier of the interest. |
| `label` | string | The public label of the interest. |
| `name` | string | The internal name of the interest. |
| `visibility` | string | Whether the interest is public or private. |

## Native endpoint

Through the native Flexmail API, this operation is `GET /interests` (base URL `https://api.flexmail.eu`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-interests.md) for the provider-specific parameters and requirements.

