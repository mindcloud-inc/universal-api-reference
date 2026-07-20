# Hex: Get Project



```
GET https://connect.mindcloud.co/v1/universal/hex/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hex/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=019d64e5-c78b-7004-a3be-4ebffc5cad3f" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "019d64e5-c78b-7004-a3be-4ebffc5cad3f"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hex/latest/actions/get-project?${params}`, {
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
| `projectId` | string | yes | Unique ID for a Hex project. Default: `019d64e5-c78b-7004-a3be-4ebffc5cad3f`. |
| `includeSharing` | boolean | no | Whether to include sharing details for the project. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analytics": {
        "appViews": {
          "allTime": 1,
          "lastFourteenDays": 1,
          "lastSevenDays": 1,
          "lastThirtyDays": 1
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
      "lastEditedAt": "2026-05-07T12:00:00.000Z",
      "lastPublishedAt": "2026-05-07T12:00:00.000Z",
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
| `analytics.appViews.lastFourteenDays` | number |  |
| `analytics.appViews.lastSevenDays` | number |  |
| `analytics.appViews.lastThirtyDays` | number |  |
| `categories` | array<object> | Creates a new project in Hex. |
| `createdAt` | date |  |
| `creator.email` | string |  |
| `description` | string |  |
| `id` | string |  |
| `lastEditedAt` | date |  |
| `lastPublishedAt` | date |  |
| `owner.email` | string |  |
| `reviews.required` | boolean |  |
| `schedules` | array<object> | Updates an existing project in Hex. |
| `sharing.collections` | array<object> | Retrieves runs for a project from Hex. |
| `sharing.groups` | array<object> | Retrieves a project run from Hex. |
| `sharing.publicWeb.access` | string |  |
| `sharing.users` | array<object> | Runs the latest published version of a project in Hex. |
| `sharing.workspace.access` | string |  |
| `status.name` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Hex API, this operation is `GET /projects/{projectId}` (base URL `https://app.hex.tech/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

