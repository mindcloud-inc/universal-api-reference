# Tableau Cloud: Publish Workbook

Publishes a workbook to Tableau Cloud.

```
POST https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/publish-workbook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tableau Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/publish-workbook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/publish-workbook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "contentUrl": "https://example.com",
      "createdAt": "string",
      "defaultViewId": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "showTabs": "string",
      "size": "string",
      "updatedAt": "string",
      "webpageUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentUrl` | string | Workbook content URL. |
| `createdAt` | string | Creation timestamp. |
| `defaultViewId` | string | Default view ID. |
| `description` | string | Workbook description. |
| `id` | string | Workbook ID. |
| `name` | string | Workbook name. |
| `showTabs` | string | Whether workbook tabs are shown. |
| `size` | string | Workbook size. |
| `updatedAt` | string | Last update timestamp. |
| `webpageUrl` | string | Workbook web URL. |

## Native endpoint

Through the native Tableau Cloud API, this operation is `POST /sites/site-id/workbooks` (base URL `https://us-east-1.online.tableau.com/api/3.28`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-workbook.md) for the provider-specific parameters and requirements.

