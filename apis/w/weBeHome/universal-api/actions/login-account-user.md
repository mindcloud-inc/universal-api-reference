# WeBeHome: Login Account User



```
POST https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/login-account-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeBeHome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/login-account-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "DeviceName": "MindCloud"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/login-account-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "DeviceName": "MindCloud"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `DeviceName` | string | yes | Name of the client device. Default: `MindCloud`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BaseUnitID": 1,
      "ClusterID": 1,
      "Created": "string",
      "jwt": "string",
      "UserType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BaseUnitID` | number |  |
| `ClusterID` | number |  |
| `Created` | string |  |
| `jwt` | string |  |
| `UserType` | string |  |

## Native endpoint

Through the native WeBeHome API, this operation is `POST OpenAPIservice.svc/CreateWebTokens/LoginAccountUser` (base URL `https://webehome.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/login-account-user.md) for the provider-specific parameters and requirements.

