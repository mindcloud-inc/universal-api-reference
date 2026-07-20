# Edoobox: Get User

Retrieves details for a user from Edoobox.

```
GET https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edoobox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=user_3ede73bbc12f_17275262932" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "user_3ede73bbc12f_17275262932"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/get-user?${params}`, {
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
| `userId` | string | yes | edoobox user ID. Default: `user_3ede73bbc12f_17275262932`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `country` | string |  |
| `data1` | string |  |
| `data10` | string |  |
| `data11` | string |  |
| `data12` | string |  |
| `data13` | string |  |
| `data14` | string |  |
| `data15` | string |  |
| `data16` | string |  |
| `data17` | string |  |
| `data18` | string |  |
| `data19` | string |  |
| `data2` | string |  |
| `data20` | string |  |
| `data21` | string |  |
| `data22` | string |  |
| `data23` | string |  |
| `data24` | string |  |
| `data25` | string |  |
| `data26` | string |  |
| `data27` | string |  |
| `data28` | string |  |
| `data29` | string |  |
| `data3` | string |  |
| `data30` | string |  |
| `data4` | string |  |
| `data5` | string |  |
| `data6` | string |  |
| `data7` | string |  |
| `data8` | string |  |
| `data9` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `gender` | string |  |
| `gid` | string |  |
| `id` | string |  |
| `language` | string |  |
| `lastName` | string |  |
| `location` | string |  |
| `master` | boolean |  |
| `phoneNumber` | string |  |
| `postcode` | string |  |
| `status` | boolean |  |
| `street` | string |  |

## Native endpoint

Through the native Edoobox API, this operation is `GET /user/:user_id` (base URL `https://app2.edoobox.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

