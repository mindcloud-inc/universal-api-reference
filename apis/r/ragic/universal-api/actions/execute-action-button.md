# Ragic: Execute Action Button

Executes an action button on a Ragic record.

```
PUT https://connect.mindcloud.co/v1/universal/ragic/latest/actions/execute-action-button
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ragic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ragic/latest/actions/execute-action-button" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tabFolderPath": "ragic-setup",
  "sheetIndex": "8",
  "recordId": "0",
  "buttonId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ragic/latest/actions/execute-action-button', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tabFolderPath": "ragic-setup",
    "sheetIndex": "8",
    "recordId": "0",
    "buttonId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tabFolderPath` | string | yes | The folder path from the Ragic URL, for example `ragic-setup`. Default: `ragic-setup`. |
| `sheetIndex` | number | yes | The sheet number from the Ragic URL. Default: `8`. |
| `recordId` | number | yes | The record ID from the Ragic record URL. Default: `0`. |
| `buttonId` | number | yes | The action-button ID returned by `List Action Buttons`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "msg": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `msg` | string | The action-button execution message from Ragic. |
| `status` | string | The action-button execution status. |

## Native endpoint

Through the native Ragic API, this operation is `POST /:tabFolderPath/:sheetIndex/:recordId` (base URL `{{credentials.serverUrl}}/mindcloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-action-button.md) for the provider-specific parameters and requirements.

