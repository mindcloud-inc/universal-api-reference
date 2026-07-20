# Erase.bg: Get App Details

Retrieves app details from Erase.bg.

```
GET https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/get-app-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Erase.bg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/get-app-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/get-app-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "app": {
        "_id": "string",
        "accessKey": "string",
        "active": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "orgId": "string",
        "permissions": [
          "string"
        ],
        "token": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "org": {
        "_id": "string",
        "active": true,
        "cloudName": "Ava Chen",
        "config": {},
        "createdAt": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "ownerId": "string",
        "restrictions": [
          "string"
        ],
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app` | object |  |
| `app._id` | string |  |
| `app.accessKey` | string |  |
| `app.active` | boolean |  |
| `app.createdAt` | date |  |
| `app.name` | string |  |
| `app.orgId` | string |  |
| `app.permissions` | array<string> |  |
| `app.token` | string |  |
| `app.updatedAt` | date |  |
| `org` | object |  |
| `org._id` | string |  |
| `org.active` | boolean |  |
| `org.cloudName` | string |  |
| `org.config` | object |  |
| `org.createdAt` | date |  |
| `org.name` | string |  |
| `org.ownerId` | string |  |
| `org.restrictions` | array<string> |  |
| `org.updatedAt` | date |  |

## Native endpoint

Through the native Erase.bg API, this operation is `GET /service/platform/organization/v1.0/apps/info` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app-details.md) for the provider-specific parameters and requirements.

