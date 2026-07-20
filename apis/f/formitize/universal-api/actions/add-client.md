# Formitize: Add Client

Creates a new client in Formitize.

```
POST https://connect.mindcloud.co/v1/universal/formitize/latest/actions/add-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formitize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formitize/latest/actions/add-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formitize/latest/actions/add-client', {
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
      "billingName": "Ava Chen",
      "contactIDs": [
        1
      ],
      "id": "string",
      "locationIDs": [
        1
      ],
      "primaryAddress": "string",
      "primaryAddressID": 1,
      "primaryContactID": 1,
      "primaryContactName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingName` | string |  |
| `contactIDs` | array<number> |  |
| `id` | string |  |
| `locationIDs` | array<number> |  |
| `primaryAddress` | string |  |
| `primaryAddressID` | number |  |
| `primaryContactID` | number |  |
| `primaryContactName` | string |  |

## Native endpoint

Through the native Formitize API, this operation is `POST /crm/client/` (base URL `https://service.formitize.com/api/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-client.md) for the provider-specific parameters and requirements.

