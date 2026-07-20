# Edoobox: Get User Dashboard

Retrieves a user dashboard from Edoobox.

```
GET https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/get-user-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edoobox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/get-user-dashboard?connectionId=$CONNECTION_ID&userId=user_3ede73bbc12f_17275262932" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "user_3ede73bbc12f_17275262932"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/get-user-dashboard?${params}`, {
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
| `userId` | string | yes | The edoobox user id. Default: `user_3ede73bbc12f_17275262932`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "barcode": {
        "code": "string",
        "id": "string",
        "type": "string"
      },
      "files": true,
      "geocode": true,
      "user": {
        "company": "string",
        "country": "string",
        "data1": "string",
        "data10": "string",
        "data11": "string",
        "data12": "string",
        "data13": "string",
        "data14": "string",
        "data15": "string",
        "data16": "string",
        "data17": "string",
        "data18": "string",
        "data19": "string",
        "data2": "string",
        "data20": "string",
        "data21": "string",
        "data22": "string",
        "data23": "string",
        "data24": "string",
        "data25": "string",
        "data26": "string",
        "data27": "string",
        "data28": "string",
        "data29": "string",
        "data3": "string",
        "data30": "string",
        "data4": "string",
        "data5": "string",
        "data6": "string",
        "data7": "string",
        "data8": "string",
        "data9": "string",
        "email": "ava@example.com",
        "firstName": "Ava",
        "gender": "string",
        "gid": "string",
        "id": "string",
        "language": "string",
        "lastName": "Chen",
        "location": "string",
        "master": true,
        "phoneNumber": "string",
        "postcode": "string",
        "status": true,
        "street": "string"
      },
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `barcode.code` | string |  |
| `barcode.id` | string |  |
| `barcode.type` | string |  |
| `files` | boolean |  |
| `geocode` | boolean |  |
| `user.company` | string |  |
| `user.country` | string |  |
| `user.data1` | string |  |
| `user.data10` | string |  |
| `user.data11` | string |  |
| `user.data12` | string |  |
| `user.data13` | string |  |
| `user.data14` | string |  |
| `user.data15` | string |  |
| `user.data16` | string |  |
| `user.data17` | string |  |
| `user.data18` | string |  |
| `user.data19` | string |  |
| `user.data2` | string |  |
| `user.data20` | string |  |
| `user.data21` | string |  |
| `user.data22` | string |  |
| `user.data23` | string |  |
| `user.data24` | string |  |
| `user.data25` | string |  |
| `user.data26` | string |  |
| `user.data27` | string |  |
| `user.data28` | string |  |
| `user.data29` | string |  |
| `user.data3` | string |  |
| `user.data30` | string |  |
| `user.data4` | string |  |
| `user.data5` | string |  |
| `user.data6` | string |  |
| `user.data7` | string |  |
| `user.data8` | string |  |
| `user.data9` | string |  |
| `user.email` | string |  |
| `user.firstName` | string |  |
| `user.gender` | string |  |
| `user.gid` | string |  |
| `user.id` | string |  |
| `user.language` | string |  |
| `user.lastName` | string |  |
| `user.location` | string |  |
| `user.master` | boolean |  |
| `user.phoneNumber` | string |  |
| `user.postcode` | string |  |
| `user.status` | boolean |  |
| `user.street` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Edoobox API, this operation is `GET /user/:user_id/dashboard` (base URL `https://app2.edoobox.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-dashboard.md) for the provider-specific parameters and requirements.

