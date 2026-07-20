# Softr: Get Table



```
GET https://connect.mindcloud.co/v1/universal/softr/latest/actions/get-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Softr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/softr/latest/actions/get-table?connectionId=$CONNECTION_ID&databaseId=string&tableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string",
  "tableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/softr/latest/actions/get-table?${params}`, {
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
| `databaseId` | string | yes | The ID of the database. |
| `tableId` | string | yes | The ID of the table. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultViewId": "string",
      "fields": [
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
          "readonly": true,
          "required": true,
          "type": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "id": "string",
      "name": "Ava Chen",
      "primaryFieldId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `defaultViewId` | string |  |
| `fields[].aiOptions.aiFillable` | boolean |  |
| `fields[].aiOptions.aiModel` | string |  |
| `fields[].aiOptions.aiOnly` | boolean |  |
| `fields[].aiOptions.allowWebSearch` | boolean |  |
| `fields[].aiOptions.canBeTriggeredManually` | boolean |  |
| `fields[].aiOptions.prompt` | string |  |
| `fields[].aiOptions.runOnUpdateMode` | string |  |
| `fields[].aiOptions.runWhenRecordIsCreated` | boolean |  |
| `fields[].aiOptions.runWhenRecordIsUpdated` | boolean |  |
| `fields[].aiOptions.skipIfValueExists` | boolean |  |
| `fields[].allowMultipleEntries` | boolean |  |
| `fields[].createdAt` | date |  |
| `fields[].id` | string |  |
| `fields[].locked` | boolean |  |
| `fields[].name` | string |  |
| `fields[].readonly` | boolean |  |
| `fields[].required` | boolean |  |
| `fields[].type` | string |  |
| `fields[].updatedAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `primaryFieldId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Softr API, this operation is `GET /databases/:databaseId/tables/:tableId` (base URL `https://tables-api.softr.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-table.md) for the provider-specific parameters and requirements.

