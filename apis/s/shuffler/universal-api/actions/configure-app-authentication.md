# Shuffler: Configure App Authentication

Updates an app authentication in Shuffler.

```
PUT https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/configure-app-authentication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/configure-app-authentication" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "authenticationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/configure-app-authentication', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "authenticationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | yes | Configuration action such as assign_everywhere or suborg_distribute. |
| `authenticationId` | string | yes | Authentication Id path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Shuffler API, this operation is `POST /apps/authentication/{authenticationId}/config` (base URL `https://shuffler.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/configure-app-authentication.md) for the provider-specific parameters and requirements.

