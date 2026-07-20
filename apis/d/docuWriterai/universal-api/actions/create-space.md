# DocuWriter.ai: Create Space



```
POST https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/create-space
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuWriter.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/create-space" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/create-space', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Space description. |
| `isPublic` | boolean | no | Whether the new Space is public. |
| `name` | string | yes | Space name. |
| `slug` | string | no | Optional URL slug for public Spaces. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "isPublic": true,
      "name": "Ava Chen",
      "slug": "string",
      "sort": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the space was created. |
| `description` | string | Space description. |
| `id` | number | Unique identifier of the space. |
| `isPublic` | boolean | Whether the space is public. |
| `name` | string | Space name. |
| `slug` | string | Public slug when available. |
| `sort` | number | Sort order for the space. |
| `userId` | number | Owner user identifier. |

## Native endpoint

Through the native DocuWriter.ai API, this operation is `POST /api/spaces` (base URL `https://app.docuwriter.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-space.md) for the provider-specific parameters and requirements.

