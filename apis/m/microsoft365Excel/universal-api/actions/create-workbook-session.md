# Microsoft 365 Excel: Create Workbook Session

Creates a workbook session in Microsoft 365 Excel.

```
POST https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/create-workbook-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Excel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/create-workbook-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "driveId": "string",
  "driveItemId": "string",
  "persistChanges": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/create-workbook-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "driveId": "string",
    "driveItemId": "string",
    "persistChanges": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `driveId` | string | yes | Drive ID from the workbook item's parentReference.driveId. |
| `driveItemId` | string | yes | Drive item ID of the Excel workbook file. |
| `persistChanges` | boolean | yes | Whether changes made in the workbook session are saved to the source workbook. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "persistChanges": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | ID of the workbook session. |
| `persistChanges` | boolean | True for a persistent session; false for a non-persistent session. |

## Native endpoint

Through the native Microsoft 365 Excel API, this operation is `POST /v1.0/drives/:driveId/items/:driveItemId/workbook/createSession` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workbook-session.md) for the provider-specific parameters and requirements.

