# CompanyHub: Update Record

Updates an existing record in a CompanyHub table.

```
PUT https://connect.mindcloud.co/v1/universal/companyHub/latest/actions/update-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/companyHub/latest/actions/update-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableName": "Contact",
  "id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/companyHub/latest/actions/update-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableName": "Contact",
    "id": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tableName` | string | yes | Exact CompanyHub API table name, for example Contact, Company, Deal, or a custom table name. Example: `Contact`. |
| `id` | string | yes | CompanyHub record ID. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "isDuplicate": true,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `isDuplicate` | boolean |  |
| `success` | boolean |  |

## Native endpoint

Through the native CompanyHub API, this operation is `PUT /tables/:tableName/:id` (base URL `https://api.companyhub.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-record.md) for the provider-specific parameters and requirements.

