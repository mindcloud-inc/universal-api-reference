# Hex: Update Project



```
PUT https://connect.mindcloud.co/v1/universal/hex/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hex/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hex/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Unique ID for a Hex project. |
| `status` | string | no | Project status value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analytics": {
        "appViews": {
          "allTime": 1
        }
      },
      "categories": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creator": {
        "email": "ava@example.com"
      },
      "description": "string",
      "id": "string",
      "owner": {
        "email": "ava@example.com"
      },
      "reviews": {
        "required": true
      },
      "schedules": [
        {}
      ],
      "sharing": {
        "collections": [
          {}
        ],
        "groups": [
          {}
        ],
        "publicWeb": {
          "access": "string"
        },
        "users": [
          {}
        ],
        "workspace": {
          "access": "string"
        }
      },
      "status": {
        "name": "Ava Chen"
      },
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analytics.appViews.allTime` | number |  |
| `categories` | array<object> | Updates an existing collection in Hex. |
| `createdAt` | date |  |
| `creator.email` | string |  |
| `description` | string |  |
| `id` | string |  |
| `owner.email` | string |  |
| `reviews.required` | boolean |  |
| `schedules` | array<object> | Retrieves groups from Hex. |
| `sharing.collections` | array<object> | Creates a new group in Hex. |
| `sharing.groups` | array<object> | Updates an existing group in Hex. |
| `sharing.publicWeb.access` | string |  |
| `sharing.users` | array<object> | Retrieves a group from Hex. |
| `sharing.workspace.access` | string |  |
| `status.name` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Hex API, this operation is `PATCH /projects/:projectId` (base URL `https://app.hex.tech/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

