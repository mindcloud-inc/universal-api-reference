# Microsoft Power BI: Get Installed App



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/get-installed-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/get-installed-app?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/get-installed-app?${params}`, {
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
| `appId` | string | yes | The installed app ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "lastUpdate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "publishedBy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | The app description. |
| `id` | string | The installed app ID. |
| `lastUpdate` | date | The date and time the app was last updated. |
| `name` | string | The app name. |
| `publishedBy` | string | The app publisher. |

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET apps/[:appId]` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-installed-app.md) for the provider-specific parameters and requirements.

