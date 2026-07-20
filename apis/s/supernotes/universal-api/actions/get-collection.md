# Supernotes: Get Collection

Retrieves a specific collection from Supernotes.

```
GET https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supernotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-collection?connectionId=$CONNECTION_ID&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-collection?${params}`, {
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
| `collectionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdWhen": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "modifiedWhen": "2026-05-07T12:00:00.000Z",
      "order": "string",
      "spec": {},
      "view": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdWhen` | date |  |
| `id` | string |  |
| `modifiedWhen` | date |  |
| `order` | string |  |
| `spec` | object |  |
| `view` | object |  |

## Native endpoint

Through the native Supernotes API, this operation is `GET /collections/:collection_id` (base URL `https://api.supernotes.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-collection.md) for the provider-specific parameters and requirements.

