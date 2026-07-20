# Tableau Cloud: Add Workbook to Favorites

Adds a workbook to favorites in Tableau Cloud.

```
POST https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/add-workbook-to-favorites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tableau Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/add-workbook-to-favorites" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/add-workbook-to-favorites', {
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
      "label": "string",
      "name": "Ava Chen",
      "updatedAt": "string",
      "viewUrlName": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentUrl` | string | Favorited item content URL. |
| `createdAt` | string | Creation timestamp. |
| `label` | string | Favorite label. |
| `name` | string | Favorited item name. |
| `updatedAt` | string | Last update timestamp. |
| `viewUrlName` | string | View URL name when applicable. |

## Native endpoint

Through the native Tableau Cloud API, this operation is `PUT /sites/site-id/favorites/user-id` (base URL `https://us-east-1.online.tableau.com/api/3.28`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-workbook-to-favorites.md) for the provider-specific parameters and requirements.

