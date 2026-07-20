# Workiom: Get App

Retrieves an app from your Workiom workspace.

```
GET https://connect.mindcloud.co/v1/universal/workiom/latest/actions/get-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workiom/latest/actions/get-app?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workiom/latest/actions/get-app?${params}`, {
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
      "creationTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "icon": "string",
      "iconUrl": "https://example.com",
      "id": "string",
      "isPublic": true,
      "lastModificationTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationTime` | date |  |
| `description` | string |  |
| `icon` | string |  |
| `iconUrl` | string |  |
| `id` | string |  |
| `isPublic` | boolean |  |
| `lastModificationTime` | date |  |
| `name` | string |  |

## Native endpoint

Through the native Workiom API, this operation is `GET /api/services/app/Apps/Get` (base URL `https://api.workiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app.md) for the provider-specific parameters and requirements.

