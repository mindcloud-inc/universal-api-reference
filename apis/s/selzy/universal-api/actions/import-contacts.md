# Selzy: Import Contacts

Imports contacts into Selzy.

```
POST https://connect.mindcloud.co/v1/universal/selzy/latest/actions/import-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Selzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/selzy/latest/actions/import-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/selzy/latest/actions/import-contacts', {
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
      "result": {
        "deleted": 1,
        "inserted": 1,
        "invalid": 1,
        "log": [
          {
            "code": "string",
            "index": 1,
            "message": "string"
          }
        ],
        "new_emails": 1,
        "total": 1,
        "updated": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result.deleted` | number |  |
| `result.inserted` | number |  |
| `result.invalid` | number |  |
| `result.log[].code` | string |  |
| `result.log[].index` | number |  |
| `result.log[].message` | string |  |
| `result.new_emails` | number |  |
| `result.total` | number |  |
| `result.updated` | number |  |

## Native endpoint

Through the native Selzy API, this operation is `POST importContacts` (base URL `https://api.selzy.com/en/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-contacts.md) for the provider-specific parameters and requirements.

