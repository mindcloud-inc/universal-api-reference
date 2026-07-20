# Rocketlane: Get User

Retrieves a user from Rocketlane.

```
GET https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/get-user?${params}`, {
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
| `userId` | number | yes | The user's unique, system-generated identifier, which can be used to identify the user globally. |
| `includeFields` | list<string> | no | This query parameter allows you to specify which fields should be returned in the response body by selecting from the drop down. To get the relevant fields, use comma separated values. If the field is left blank, the default properties are returned. |
| `includeAllFields` | boolean | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capacityInMinutes": 1,
      "company": {},
      "createdAt": 1,
      "createdBy": {},
      "email": "ava@example.com",
      "fields": [
        {}
      ],
      "firstName": "Ava",
      "holidayCalendar": {},
      "lastName": "Chen",
      "permission": {},
      "profilePictureUrl": "https://example.com",
      "role": {},
      "status": "string",
      "type": "string",
      "updatedAt": 1,
      "updatedBy": {},
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capacityInMinutes` | number | The capacity of user, should be multiples of 5, default value is capacity configured in profile. |
| `company` | object | The company of the user. |
| `createdAt` | number | The time when the user was created. The referenced time will be in epoch millis. |
| `createdBy` | object | The team member who updated the information of the user. |
| `email` | string | The email identifier of the user. |
| `fields` | array<object> | Custom user fields can be created and their values set during user creation. These values can also be added or edited later. The field value can be a string, number, or array, and must align with the field type. Refer [e xamples](https://developer.rocketlane.com/v1.0/docs/custom-fields#examples-of-requests-and-responses-for-assigning-custom-field-values) to know how each `field_type` is associated with user. |
| `firstName` | string | The first name of the user. |
| `holidayCalendar` | object | The Holiday calendar of the user. |
| `lastName` | string | The last name of the user. |
| `permission` | object | The Permission of the user. |
| `profilePictureUrl` | string | The URL of the user's profile picture. |
| `role` | object | The role of the user. |
| `status` | string | The status of the user. |
| `type` | string | The type of the user. |
| `updatedAt` | number | The time when the user's information was updated. Any changes that's related to the user are captured and specified here in epoch millis. |
| `updatedBy` | object | The team member who updated the information of the user. |
| `userId` | number | The user's unique, system-generated identifier, which can be used to identify the user globally. |

## Native endpoint

Through the native Rocketlane API, this operation is `GET /1.0/users/:userId` (base URL `https://api.rocketlane.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

