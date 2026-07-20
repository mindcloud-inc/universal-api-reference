# Cryptlex: Get Release

Retrieves a release from Cryptlex.

```
GET https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/get-release
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptlex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/get-release?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/get-release?${params}`, {
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

Through the native Cryptlex API, this operation is `GET /v3/releases/:id` (base URL `https://api.cryptlex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-release.md) for the provider-specific parameters and requirements.

