# Priority: Get User

Retrieves a user from Priority.

```
GET https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-user?connectionId=$CONNECTION_ID&userLogin=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userLogin": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-user?${params}`, {
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
| `userLogin` | string | yes | Priority user login key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "GROUPNAME": "Ava Chen",
      "SNAME": "Ava Chen",
      "USERID": 1,
      "USERLOGIN": "string",
      "USERNAME": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `GROUPNAME` | string |  |
| `SNAME` | string |  |
| `USERID` | number |  |
| `USERLOGIN` | string |  |
| `USERNAME` | string |  |

## Native endpoint

Through the native Priority API, this operation is `GET /USERS(USERLOGIN=':userLogin')` (base URL `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

