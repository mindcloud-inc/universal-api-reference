# Kiwili: Update Enterprise

Updates an existing enterprise in Kiwili.

```
PUT https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/update-enterprise
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/update-enterprise" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "enterprise_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/update-enterprise', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "enterprise_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `enterprise_id` | number | yes | The Kiwili enterprise ID to update. |
| `IsClient` | boolean | no | Whether the enterprise is a client. |
| `Name` | string | no | The updated enterprise name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Active": true,
      "Email": "ava@example.com",
      "Id": 1,
      "IsClient": true,
      "Name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Active` | boolean |  |
| `Email` | string |  |
| `Id` | number |  |
| `IsClient` | boolean |  |
| `Name` | string |  |

## Native endpoint

Through the native Kiwili API, this operation is `PUT /enterprise/:enterprise_id` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-enterprise.md) for the provider-specific parameters and requirements.

