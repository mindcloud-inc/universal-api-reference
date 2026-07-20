# Hex: Create Project



```
POST https://connect.mindcloud.co/v1/universal/hex/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hex/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hex/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Project description. |
| `title` | string | yes | Project title. |

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
| `categories` | array<object> | Cancels a project run in Hex. |
| `createdAt` | date |  |
| `creator.email` | string |  |
| `description` | string |  |
| `id` | string |  |
| `owner.email` | string |  |
| `reviews.required` | boolean |  |
| `schedules` | array<object> | Creates a presigned embed URL for a project in Hex. |
| `sharing.collections` | array<object> | Retrieves a collection from Hex. |
| `sharing.groups` | array<object> | Creates a new collection in Hex. |
| `sharing.publicWeb.access` | string |  |
| `sharing.users` | array<object> | Retrieves collections from Hex. |
| `sharing.workspace.access` | string |  |
| `status.name` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Hex API, this operation is `POST /projects` (base URL `https://app.hex.tech/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

