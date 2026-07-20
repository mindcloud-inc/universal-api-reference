# Global Patron: Create Datalist

Creates a datalist in Global Patron.

```
POST https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/create-datalist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Patron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/create-datalist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/create-datalist', {
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
      "createdDateUtc": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "modifiedDateUtc": "2026-05-07T12:00:00.000Z",
      "settings": {
        "listDescription": "string",
        "listName": "Ava Chen",
        "listType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDateUtc` | date | Creation timestamp. |
| `id` | string | Datalist identifier. |
| `modifiedDateUtc` | date | Last modification timestamp. |
| `settings` | object | Datalist settings. |
| `settings.listDescription` | string | Datalist description. |
| `settings.listName` | string | Datalist name. |
| `settings.listType` | string | Datalist type. |

## Native endpoint

Through the native Global Patron API, this operation is `POST /api/restricted/datalist` (base URL `https://api.globalpatron.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-datalist.md) for the provider-specific parameters and requirements.

