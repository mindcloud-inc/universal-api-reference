# Microsoft Power BI: List Dashboards in Workspace



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-dashboards-in-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-dashboards-in-workspace?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-dashboards-in-workspace?${params}`, {
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
| `groupId` | string | yes | The workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "displayName": "Ava Chen",
      "embedUrl": "https://example.com",
      "id": "string",
      "isReadOnly": true,
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string | The app ID when the dashboard belongs to an app. |
| `displayName` | string | The dashboard display name. |
| `embedUrl` | string | The embed URL of the dashboard. |
| `id` | string | The dashboard ID. |
| `isReadOnly` | boolean | Whether the dashboard is read-only. |
| `webUrl` | string | The web URL of the dashboard. |

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET groups/[:groupId]/dashboards` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dashboards-in-workspace.md) for the provider-specific parameters and requirements.

