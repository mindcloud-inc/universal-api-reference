# Quickbase: Get App

Retrieves a Quickbase app by ID.

```
GET https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/get-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quickbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/get-app?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/get-app?${params}`, {
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
| `appId` | string | yes | The Quickbase app identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "dateFormat": "string",
      "description": "string",
      "hasEveryoneOnTheInternet": true,
      "id": "string",
      "memoryInfo": {},
      "name": "Ava Chen",
      "securityProperties": {},
      "timeZone": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | When the app was created. |
| `dateFormat` | string | The app date format. |
| `description` | string | The application description. |
| `hasEveryoneOnTheInternet` | boolean | Whether the app is visible to everyone on the internet. |
| `id` | string | The Quickbase app identifier. |
| `memoryInfo` | object | Quickbase memory information for the app. |
| `name` | string | The application name. |
| `securityProperties` | object | Quickbase security settings for the app. |
| `timeZone` | string | The app time zone. |
| `updated` | date | When the app was last updated. |

## Native endpoint

Through the native Quickbase API, this operation is `GET v1/apps/:appId` (base URL `https://api.quickbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app.md) for the provider-specific parameters and requirements.

