# Exa: List Webset Items

Retrieves webset items from Exa.

```
GET https://connect.mindcloud.co/v1/universal/exa/latest/actions/list-webset-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exa/latest/actions/list-webset-items?connectionId=$CONNECTION_ID&limit=25&offset=0&webset=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "webset": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exa/latest/actions/list-webset-items?${params}`, {
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
| `webset` | string | yes | The id or externalId of the Webset |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceId` | string | no | The id of the source |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "hasMore": "string",
      "nextCursor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |
| `hasMore` | string |  |
| `nextCursor` | string |  |

## Native endpoint

Through the native Exa API, this operation is `GET /websets/v0/websets/:webset/items` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webset-items.md) for the provider-specific parameters and requirements.

