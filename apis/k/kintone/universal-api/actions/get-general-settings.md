# Kintone: Get General Settings

Retrieves general app settings from Kintone.

```
GET https://connect.mindcloud.co/v1/universal/kintone/latest/actions/get-general-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kintone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kintone/latest/actions/get-general-settings?connectionId=$CONNECTION_ID&appId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kintone/latest/actions/get-general-settings?${params}`, {
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
| `appId` | number | yes | The Kintone app ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language` | string | no | Optional language code used for localized settings. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "enableBulkDeletion": true,
      "enableComments": true,
      "enableDuplicateRecord": true,
      "enableInlineRecordEditing": true,
      "enableThumbnails": true,
      "firstMonthOfFiscalYear": 1,
      "icon": {},
      "name": "Ava Chen",
      "numberPrecision": 1,
      "revision": "string",
      "theme": {},
      "titleField": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `enableBulkDeletion` | boolean |  |
| `enableComments` | boolean |  |
| `enableDuplicateRecord` | boolean |  |
| `enableInlineRecordEditing` | boolean |  |
| `enableThumbnails` | boolean |  |
| `firstMonthOfFiscalYear` | number |  |
| `icon` | object |  |
| `name` | string |  |
| `numberPrecision` | number |  |
| `revision` | string |  |
| `theme` | object |  |
| `titleField` | string |  |

## Native endpoint

Through the native Kintone API, this operation is `GET /app/settings.json` (base URL `{{credentials.baseUrl}}/k/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-general-settings.md) for the provider-specific parameters and requirements.

