# MailUp: Get Import

Retrieves an import job from MailUp.

```
GET https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/get-import
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/get-import?connectionId=$CONNECTION_ID&idImport=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idImport": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/get-import?${params}`, {
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
| `idImport` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDate": "string",
      "fieldSeparator": "string",
      "filename": "Ava Chen",
      "idGroups": [
        1
      ],
      "idImport": 1,
      "idList": 1,
      "ignoreDoubleQuotes": true,
      "ignoreFirstRow": true,
      "importAsUnsubscribed": true,
      "includePendingRecipients": true,
      "overwriteEmptyFields": true,
      "replaceExistingGroup": true,
      "rows": {},
      "sendConfirmationEmail": true,
      "startDate": "string",
      "statusCode": 1,
      "stopDate": "string",
      "textDelimiter": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDate` | string |  |
| `fieldSeparator` | string |  |
| `filename` | string |  |
| `idGroups` | array<number> |  |
| `idImport` | number |  |
| `idList` | number |  |
| `ignoreDoubleQuotes` | boolean |  |
| `ignoreFirstRow` | boolean |  |
| `importAsUnsubscribed` | boolean |  |
| `includePendingRecipients` | boolean |  |
| `overwriteEmptyFields` | boolean |  |
| `replaceExistingGroup` | boolean |  |
| `rows` | object |  |
| `sendConfirmationEmail` | boolean |  |
| `startDate` | string |  |
| `statusCode` | number |  |
| `stopDate` | string |  |
| `textDelimiter` | string |  |

## Native endpoint

Through the native MailUp API, this operation is `GET Console/Imports/:id_Import` (base URL `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-import.md) for the provider-specific parameters and requirements.

