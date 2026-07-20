# Microsoft Power BI: List Installed Apps



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-installed-apps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-installed-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-installed-apps?${params}`, {
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

Through the native Microsoft Power BI API, this operation is `GET apps` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-installed-apps.md) for the provider-specific parameters and requirements.

