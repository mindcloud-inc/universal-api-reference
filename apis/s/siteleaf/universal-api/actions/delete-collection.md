# Siteleaf: Delete Collection

Deletes an existing collection from Siteleaf.

```
DELETE https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/delete-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Siteleaf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/delete-collection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/delete-collection?${params}`, {
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
| `collectionPath` | string | no | Collection path slug |
| `siteId` | string | no | Siteleaf site identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `id` | string |  |

## Native endpoint

Through the native Siteleaf API, this operation is `DELETE /sites/:site_id/collections/:path` (base URL `https://api.siteleaf.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-collection.md) for the provider-specific parameters and requirements.

