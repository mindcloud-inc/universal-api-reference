# Algolia: List Indices

Retrieves all indices in the Algolia application.

```
GET https://connect.mindcloud.co/v1/universal/algolia/latest/actions/list-indices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/list-indices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algolia/latest/actions/list-indices?${params}`, {
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
| `page` | number | no | Page of indices to retrieve. |
| `hitsPerPage` | number | no | Maximum number of indices to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "nbPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `nbPages` | number |  |

## Native endpoint

Through the native Algolia API, this operation is `GET /1/indexes` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-indices.md) for the provider-specific parameters and requirements.

