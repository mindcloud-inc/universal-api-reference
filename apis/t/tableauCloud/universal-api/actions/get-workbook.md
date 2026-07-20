# Tableau Cloud: Get Workbook

Retrieves a workbook from Tableau Cloud.

```
GET https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/get-workbook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tableau Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/get-workbook?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/get-workbook?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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

Through the native Tableau Cloud API, this operation is `GET /sites/site-id/workbooks/workbook-id` (base URL `https://us-east-1.online.tableau.com/api/3.28`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workbook.md) for the provider-specific parameters and requirements.

