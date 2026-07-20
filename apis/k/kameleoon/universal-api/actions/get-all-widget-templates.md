# Kameleoon: Get all widget templates



```
GET https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-widget-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kameleoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-widget-templates?connectionId=$CONNECTION_ID&paramsIo=page%3D1%2C%20perPage%3D20" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paramsIo": "page=1, perPage=20"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-widget-templates?${params}`, {
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
| `paramsIo` | string | yes | Required query object documented by Kameleoon for list endpoints. Example: `page=1, perPage=20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": "string",
      "cssCode": "string",
      "dateActivated": "2026-05-07T12:00:00.000Z",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateModified": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "htmlCode": "string",
      "id": 1,
      "isCustomTemplate": true,
      "name": "Ava Chen",
      "siteId": 1,
      "status": "string",
      "tags": [
        "string"
      ],
      "templateCssCode": "string",
      "templateHtmlCode": "string",
      "templateJavaScriptCode": "string",
      "themeId": 1,
      "type": "string",
      "url": "https://example.com",
      "useCustomData": true,
      "widgetEditorTemplate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | string |  |
| `cssCode` | string |  |
| `dateActivated` | date |  |
| `dateCreated` | date |  |
| `dateModified` | date |  |
| `description` | string |  |
| `htmlCode` | string |  |
| `id` | number |  |
| `isCustomTemplate` | boolean |  |
| `name` | string |  |
| `siteId` | number |  |
| `status` | string |  |
| `tags` | array<string> |  |
| `templateCssCode` | string |  |
| `templateHtmlCode` | string |  |
| `templateJavaScriptCode` | string |  |
| `themeId` | number |  |
| `type` | string |  |
| `url` | string |  |
| `useCustomData` | boolean |  |
| `widgetEditorTemplate` | string |  |

## Native endpoint

Through the native Kameleoon API, this operation is `GET templates` (base URL `https://api.kameleoon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-widget-templates.md) for the provider-specific parameters and requirements.

