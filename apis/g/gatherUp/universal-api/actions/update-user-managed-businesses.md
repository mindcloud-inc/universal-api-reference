# GatherUp: Update User Managed Businesses

Updates a user's managed businesses in GatherUp.

```
PUT https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/update-user-managed-businesses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/update-user-managed-businesses" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/update-user-managed-businesses', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessId{N}` | number | no | Managed business id. |
| `userId` | number | yes | Manager id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorCode": 1,
      "errorMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorCode` | number |  |
| `errorMessage` | string |  |

## Native endpoint

Through the native GatherUp API, this operation is `POST /user/update-managed-businesses` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-managed-businesses.md) for the provider-specific parameters and requirements.

