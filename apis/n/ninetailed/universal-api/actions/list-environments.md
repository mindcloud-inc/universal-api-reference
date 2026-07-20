# Ninetailed: List Environments



```
GET https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/list-environments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninetailed `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/list-environments?connectionId=$CONNECTION_ID&limit=25&offset=0&spaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "spaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/list-environments?${params}`, {
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
| `spaceId` | string | yes | Contentful space ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "sys": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `sys` | object |  |

## Native endpoint

Through the native Ninetailed API, this operation is `GET /spaces/:space_id/environments` (base URL `https://api.contentful.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-environments.md) for the provider-specific parameters and requirements.

