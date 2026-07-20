# Microsoft Power BI: List Reports in Installed App



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-reports-in-installed-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-reports-in-installed-app?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-reports-in-installed-app?${params}`, {
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
      "appId": "string",
      "datasetId": "string",
      "description": "string",
      "embedUrl": "https://example.com",
      "format": "string",
      "id": "string",
      "isOwnedByMe": true,
      "name": "Ava Chen",
      "originalReportId": "string",
      "reportType": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string | The app ID when the report belongs to an app. |
| `datasetId` | string | The dataset ID of the report. |
| `description` | string | The report description. |
| `embedUrl` | string | The embed URL of the report. |
| `format` | string | The report definition format type. |
| `id` | string | The report ID. |
| `isOwnedByMe` | boolean | Whether the current user can modify or copy the report. |
| `name` | string | The report name. |
| `originalReportId` | string | The original report ID when published as an app. |
| `reportType` | string | The report type. |
| `webUrl` | string | The web URL of the report. |

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET apps/[:appId]/reports` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reports-in-installed-app.md) for the provider-specific parameters and requirements.

