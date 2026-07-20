# GatherUp: List Users

Retrieves a list of users from GatherUp.

```
GET https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-users?${params}`, {
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
| `email` | string | no | Search by email token. |
| `page` | number | no | Page. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "errorCode": 1,
      "errorMessage": "string",
      "page": 1,
      "pages": 1,
      "perPage": 1,
      "userEmail": "ava@example.com",
      "userFirstName": "Ava",
      "userId": "string",
      "userLastName": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `errorCode` | number |  |
| `errorMessage` | string |  |
| `page` | number |  |
| `pages` | number |  |
| `perPage` | number |  |
| `userEmail` | string |  |
| `userFirstName` | string |  |
| `userId` | string |  |
| `userLastName` | string |  |

## Native endpoint

Through the native GatherUp API, this operation is `POST /user/managers/get` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

