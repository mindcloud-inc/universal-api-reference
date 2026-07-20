# CompanyHub: Create Record

Creates a new record in a CompanyHub table.

```
POST https://connect.mindcloud.co/v1/universal/companyHub/latest/actions/create-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/companyHub/latest/actions/create-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableName": "Contact"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/companyHub/latest/actions/create-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableName": "Contact"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tableName` | string | yes | Exact CompanyHub API table name, for example Contact, Company, Deal, or a custom table name. Example: `Contact`. |

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

Through the native CompanyHub API, this operation is `POST /tables/:tableName` (base URL `https://api.companyhub.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-record.md) for the provider-specific parameters and requirements.

