# Microsoft 365: Create Worksheet in Workbook

Creates a worksheet in a Microsoft 365 workbook.

```
POST https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/create-worksheet-in-workbook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/create-worksheet-in-workbook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "driveItemId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/create-worksheet-in-workbook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "driveItemId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `driveItemId` | string | yes | Drive item ID of the workbook file. |
| `name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@odata": {
        "context": "string",
        "id": "string"
      },
      "id": "string",
      "name": "Ava Chen",
      "position": 1,
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@odata.context` | string |  |
| `@odata.id` | string |  |
| `id` | string |  |
| `name` | string |  |
| `position` | number |  |
| `visibility` | string |  |

## Native endpoint

Through the native Microsoft 365 API, this operation is `POST /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-worksheet-in-workbook.md) for the provider-specific parameters and requirements.

