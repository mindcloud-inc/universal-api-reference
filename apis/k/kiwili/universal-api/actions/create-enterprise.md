# Kiwili: Create Enterprise

Creates a new enterprise in Kiwili.

```
POST https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/create-enterprise
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/create-enterprise" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/create-enterprise', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Email` | string | no | Primary email address for the enterprise. |
| `IsClient` | boolean | no | Whether the enterprise is a client. |
| `Name` | string | yes | The enterprise name. |

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

Through the native Kiwili API, this operation is `POST /enterprise` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-enterprise.md) for the provider-specific parameters and requirements.

