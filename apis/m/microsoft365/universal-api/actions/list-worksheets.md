# Microsoft 365: List Worksheets

Retrieves worksheets from a Microsoft 365 workbook.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-worksheets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-worksheets?connectionId=$CONNECTION_ID&driveItemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "driveItemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-worksheets?${params}`, {
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
| `driveItemId` | string | yes | Drive item ID of the Excel workbook file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@odata": {
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
| `@odata.id` | string |  |
| `id` | string |  |
| `name` | string |  |
| `position` | number |  |
| `visibility` | string |  |

## Native endpoint

Through the native Microsoft 365 API, this operation is `GET /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-worksheets.md) for the provider-specific parameters and requirements.

