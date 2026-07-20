# Dify: Get App WebApp Settings

Retrieves WebApp settings from Dify.

```
GET https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-app-webapp-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-app-webapp-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-app-webapp-settings?${params}`, {
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
      "chatColorTheme": "string",
      "chatColorThemeInverted": true,
      "copyright": "string",
      "customDisclaimer": "string",
      "defaultLanguage": "string",
      "description": "string",
      "icon": "string",
      "iconBackground": "string",
      "iconType": "string",
      "iconUrl": "https://example.com",
      "privacyPolicy": "string",
      "showWorkflowSteps": true,
      "title": "string",
      "useIconAsAnswerIcon": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chatColorTheme` | string |  |
| `chatColorThemeInverted` | boolean |  |
| `copyright` | string |  |
| `customDisclaimer` | string |  |
| `defaultLanguage` | string |  |
| `description` | string |  |
| `icon` | string |  |
| `iconBackground` | string |  |
| `iconType` | string |  |
| `iconUrl` | string |  |
| `privacyPolicy` | string |  |
| `showWorkflowSteps` | boolean |  |
| `title` | string |  |
| `useIconAsAnswerIcon` | boolean |  |

## Native endpoint

Through the native Dify API, this operation is `GET /site` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app-webapp-settings.md) for the provider-specific parameters and requirements.

