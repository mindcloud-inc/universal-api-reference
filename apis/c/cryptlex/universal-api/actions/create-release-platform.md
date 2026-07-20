# Cryptlex: Create Release Platform

Creates a release platform in Cryptlex.

```
POST https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/create-release-platform
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptlex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/create-release-platform" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "displayName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/create-release-platform', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "displayName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Platform name. |
| `displayName` | string | yes | Platform display name. |
| `description` | string | no | Platform description. |
| `productIds[]` | array<string> | no | Product IDs to associate with the release platform. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "displayName": "Ava Chen",
      "id": "string",
      "name": "Ava Chen",
      "productId": "string",
      "productIds": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `displayName` | string |  |
| `id` | string |  |
| `name` | string |  |
| `productId` | string |  |
| `productIds` | array<string> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Cryptlex API, this operation is `POST /v3/release-platforms` (base URL `https://api.cryptlex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-release-platform.md) for the provider-specific parameters and requirements.

