# Softr: Get Table Field



```
GET https://connect.mindcloud.co/v1/universal/softr/latest/actions/get-table-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Softr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/softr/latest/actions/get-table-field?connectionId=$CONNECTION_ID&databaseId=string&tableId=string&fieldId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string",
  "tableId": "string",
  "fieldId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/softr/latest/actions/get-table-field?${params}`, {
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
| `databaseId` | string | yes |  |
| `tableId` | string | yes |  |
| `fieldId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aiOptions": {
        "aiFillable": true,
        "aiModel": "string",
        "aiOnly": true,
        "allowWebSearch": true,
        "canBeTriggeredManually": true,
        "prompt": "string",
        "runOnUpdateMode": "string",
        "runWhenRecordIsCreated": true,
        "runWhenRecordIsUpdated": true,
        "skipIfValueExists": true
      },
      "allowMultipleEntries": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "locked": true,
      "name": "Ava Chen",
      "options": {
        "maxLength": 1,
        "minLength": 1
      },
      "readonly": true,
      "required": true,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiOptions.aiFillable` | boolean |  |
| `aiOptions.aiModel` | string |  |
| `aiOptions.aiOnly` | boolean |  |
| `aiOptions.allowWebSearch` | boolean |  |
| `aiOptions.canBeTriggeredManually` | boolean |  |
| `aiOptions.prompt` | string |  |
| `aiOptions.runOnUpdateMode` | string |  |
| `aiOptions.runWhenRecordIsCreated` | boolean |  |
| `aiOptions.runWhenRecordIsUpdated` | boolean |  |
| `aiOptions.skipIfValueExists` | boolean |  |
| `allowMultipleEntries` | boolean |  |
| `createdAt` | date |  |
| `id` | string |  |
| `locked` | boolean |  |
| `name` | string |  |
| `options.maxLength` | number |  |
| `options.minLength` | number |  |
| `readonly` | boolean |  |
| `required` | boolean |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Softr API, this operation is `GET /databases/:databaseId/tables/:tableId/fields/:fieldId` (base URL `https://tables-api.softr.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-table-field.md) for the provider-specific parameters and requirements.

