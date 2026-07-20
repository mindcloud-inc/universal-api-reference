# Pantry: Update Pantry Details

Updates pantry details in Pantry.

```
PUT https://connect.mindcloud.co/v1/universal/pantry/latest/actions/update-pantry-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pantry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pantry/latest/actions/update-pantry-details" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pantry/latest/actions/update-pantry-details', {
  method: 'PUT',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Updated pantry name. Example: `Mindcloud`. |
| `description` | string | no | Updated pantry description. Example: `defaultDescription`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baskets": [
        {}
      ],
      "description": "string",
      "errors": [
        "string"
      ],
      "name": "Ava Chen",
      "notifications": true,
      "percentFull": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baskets` | array<object> |  |
| `description` | string |  |
| `errors` | array<string> |  |
| `name` | string |  |
| `notifications` | boolean |  |
| `percentFull` | number |  |

## Native endpoint

Through the native Pantry API, this operation is `PUT /pantry/:pantryId` (base URL `https://getpantry.cloud/apiv1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-pantry-details.md) for the provider-specific parameters and requirements.

