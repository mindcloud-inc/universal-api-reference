# MindCloud: Create Company



```
POST https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MindCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "ACME Corp."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "ACME Corp."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Example: `ACME Corp.`. |
| `description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createdOn": "string",
        "description": "string",
        "id": "string",
        "isDeleted": {},
        "isPersonal": true,
        "name": "Ava Chen",
        "timezone": {},
        "updatedOn": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.createdOn` | string |  |
| `data.description` | string |  |
| `data.id` | string |  |
| `data.isDeleted` | object |  |
| `data.isPersonal` | boolean |  |
| `data.name` | string |  |
| `data.timezone` | object |  |
| `data.updatedOn` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native MindCloud API, this operation is `POST v1/companies` (base URL `https://embedded.mindcloud.co/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

