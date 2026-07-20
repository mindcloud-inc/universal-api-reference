# Cryptlex: Publish Release

Publishes a release in Cryptlex.

```
PUT https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/publish-release
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptlex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/publish-release" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/publish-release', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique identifier for the release. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "private": true,
      "productId": "string",
      "published": true,
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "totalFiles": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `private` | boolean |  |
| `productId` | string |  |
| `published` | boolean |  |
| `publishedAt` | date |  |
| `totalFiles` | number |  |
| `updatedAt` | date |  |
| `version` | string |  |

## Native endpoint

Through the native Cryptlex API, this operation is `POST /v3/releases/:id/publish` (base URL `https://api.cryptlex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-release.md) for the provider-specific parameters and requirements.

