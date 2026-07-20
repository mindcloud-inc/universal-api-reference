# Reteach: Get Course



```
GET https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reteach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-course?connectionId=$CONNECTION_ID&courseId=ee7eca39-ac77-424f-b3ad-53f8366fdfc6" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "courseId": "ee7eca39-ac77-424f-b3ad-53f8366fdfc6"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-course?${params}`, {
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
| `courseId` | string | yes | The id of the course. Default: `ee7eca39-ac77-424f-b3ad-53f8366fdfc6`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "description": "string",
      "editUrl": "https://example.com",
      "endsAt": "string",
      "id": "string",
      "image": {},
      "isArchived": true,
      "isDraft": true,
      "isPublic": true,
      "isWaitlistEnabled": true,
      "name": "Ava Chen",
      "participationLimit": 1,
      "startsAt": "string",
      "status": "string",
      "type": "string",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `description` | string |  |
| `editUrl` | string |  |
| `endsAt` | string |  |
| `id` | string |  |
| `image` | object |  |
| `isArchived` | boolean |  |
| `isDraft` | boolean |  |
| `isPublic` | boolean |  |
| `isWaitlistEnabled` | boolean |  |
| `name` | string |  |
| `participationLimit` | number |  |
| `startsAt` | string |  |
| `status` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Reteach API, this operation is `GET /course/{courseId}` (base URL `https://api.reteach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-course.md) for the provider-specific parameters and requirements.

