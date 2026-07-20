# Clappia: Update Workplace User Role

Updates workplace user role assignments in Clappia.

```
PUT https://connect.mindcloud.co/v1/universal/clappia/latest/actions/update-workplace-user-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clappia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/update-workplace-user-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "role": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clappia/latest/actions/update-workplace-user-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "role": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailAddress` | string | no | Email address of the workplace user to update. |
| `phoneNumber` | string | no | Phone number of the workplace user to update. |
| `role` | string | yes | Target Clappia workplace role. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clappia API returns.

## Native endpoint

Through the native Clappia API, this operation is `POST /workplace/updateWorkplaceUserRole` (base URL `https://api-public-v4.clappia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workplace-user-role.md) for the provider-specific parameters and requirements.

