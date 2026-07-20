# WeBeHome: Create Device Token



```
POST https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/create-device-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeBeHome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/create-device-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "DeviceName": "MindCloud",
  "LanguageID": "2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/create-device-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "DeviceName": "MindCloud",
    "LanguageID": "2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `DeviceName` | string | yes | Name of the client device. Default: `MindCloud`. |
| `LanguageID` | string | yes | Language identifier. Default: `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `Created` | string |  |
| `jwt` | string |  |
| `UserType` | string |  |

## Native endpoint

Through the native WeBeHome API, this operation is `POST OpenAPIservice.svc/CreateWebTokens/CreateDevice` (base URL `https://webehome.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-device-token.md) for the provider-specific parameters and requirements.

