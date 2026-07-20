# Global Patron: Update Datalist

Updates a datalist in Global Patron.

```
PUT https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/update-datalist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Patron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/update-datalist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datalistId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/update-datalist', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datalistId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datalistId` | string | yes | ID of the datalist. |

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

Through the native Global Patron API, this operation is `POST /api/restricted/datalist/{datalistId}` (base URL `https://api.globalpatron.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-datalist.md) for the provider-specific parameters and requirements.

