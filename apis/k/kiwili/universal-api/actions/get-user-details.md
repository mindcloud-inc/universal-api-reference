# Kiwili: Get User Details

Retrieves details for a user in Kiwili.

```
GET https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-user-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-user-details?connectionId=$CONNECTION_ID&user_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "user_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-user-details?${params}`, {
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
| `user_id` | number | yes | The Kiwili user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Email": "ava@example.com",
      "FirstName": "Ava",
      "FullName": "Ava Chen",
      "Id": 1,
      "LastName": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Email` | string |  |
| `FirstName` | string |  |
| `FullName` | string |  |
| `Id` | number |  |
| `LastName` | string |  |

## Native endpoint

Through the native Kiwili API, this operation is `GET /user/:user_id` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-details.md) for the provider-specific parameters and requirements.

