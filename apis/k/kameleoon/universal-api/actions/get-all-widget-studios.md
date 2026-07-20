# Kameleoon: Get all widget studios



```
GET https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-widget-studios
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kameleoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-widget-studios?connectionId=$CONNECTION_ID&paramsIo=page%3D1%2C%20perPage%3D20" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paramsIo": "page=1, perPage=20"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-widget-studios?${params}`, {
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
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateModified": "2026-05-07T12:00:00.000Z",
      "defaultLanguageId": "string",
      "elements": [
        "string"
      ],
      "enabled": true,
      "eventActions": [
        "string"
      ],
      "eventConditions": [
        "string"
      ],
      "fonts": [
        {}
      ],
      "id": "string",
      "isLegacy": true,
      "languages": [
        {}
      ],
      "name": "Ava Chen",
      "screens": [
        {}
      ],
      "templateName": "Ava Chen",
      "translation": {},
      "version": 1,
      "widgetId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | date |  |
| `dateModified` | date |  |
| `defaultLanguageId` | string |  |
| `elements` | array<string> |  |
| `enabled` | boolean |  |
| `eventActions` | array<string> |  |
| `eventConditions` | array<string> |  |
| `fonts` | array<object> |  |
| `id` | string |  |
| `isLegacy` | boolean |  |
| `languages` | array<object> |  |
| `name` | string |  |
| `screens` | array<object> |  |
| `templateName` | string |  |
| `translation` | object |  |
| `version` | number |  |
| `widgetId` | number |  |

## Native endpoint

Through the native Kameleoon API, this operation is `GET widget-studio` (base URL `https://api.kameleoon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-widget-studios.md) for the provider-specific parameters and requirements.

