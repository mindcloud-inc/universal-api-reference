# Connecteam: List User Unavailabilities

Retrieve a list of user unavailabilities, approved time-off requests and assigned shifts

```
GET https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-user-unavailabilities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Connecteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-user-unavailabilities?connectionId=$CONNECTION_ID&userId=1&startTime=1&endTime=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "1",
  "startTime": "1",
  "endTime": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-user-unavailabilities?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | number | yes |  |
| `startTime` | number | yes |  |
| `endTime` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "userUnavailabilities": [
          "string"
        ]
      },
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.userUnavailabilities` | array |  |
| `requestId` | string |  |

## Native endpoint

Through the native Connecteam API, this operation is `GET /scheduler/v1/schedulers/user-unavailability` (base URL `https://api.connecteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-unavailabilities.md) for the provider-specific parameters and requirements.

