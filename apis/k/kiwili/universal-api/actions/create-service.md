# Kiwili: Create Service

Creates a new service in Kiwili.

```
POST https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/create-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/create-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Name": "Ava Chen",
  "Rate": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/create-service', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Name": "Ava Chen",
    "Rate": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Active` | boolean | no | Whether the service is active. |
| `Billable` | boolean | no | Whether the service is billable. |
| `Name` | string | yes | The service name. |
| `Rate` | number | yes | The hourly or fixed rate for the service. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Active": true,
      "Billable": true,
      "Id": 1,
      "Name": "Ava Chen",
      "Rate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Active` | boolean |  |
| `Billable` | boolean |  |
| `Id` | number |  |
| `Name` | string |  |
| `Rate` | number |  |

## Native endpoint

Through the native Kiwili API, this operation is `POST /service` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-service.md) for the provider-specific parameters and requirements.

