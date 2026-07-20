# OfficeMaps: Create Person

Creates a new person in OfficeMaps.

```
POST https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/create-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeMaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/create-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/create-person', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `badgeNumber` | string | no | Badge number. |
| `displayName` | string | no | Preferred display name. |
| `doNotSendNewPasswordEmail` | boolean | no | Skip the new password email. |
| `email` | string | no | Person email address. |
| `employeeId` | string | no | External employee ID. |
| `firstName` | string | no | Person first name. |
| `isAllowOTPLogin` | boolean | no | Allow one-time-password login. |
| `isExcludeFromStatusNotifications` | boolean | no | Exclude from status notifications. |
| `isHiddenFromUsers` | boolean | no | Hide the person from users. |
| `lastName` | string | no | Person last name. |
| `personTypeId` | number | no | OfficeMaps person type ID. |
| `phone` | string | no | Person phone number. |
| `phoneExt` | string | no | Person phone extension. |
| `position` | string | no | Person position or role. |
| `timezoneId` | string | no | Timezone UUID. |
| `userName` | string | no | Person user name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failure": true,
      "messages": [
        "string"
      ],
      "notFound": true,
      "success": true,
      "unauthorized": true,
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failure` | boolean | Whether the request failed. |
| `messages` | array<string> | Provider messages when returned. |
| `notFound` | boolean | Whether the target record was not found. |
| `success` | boolean | Whether the request succeeded. |
| `unauthorized` | boolean | Whether the request was unauthorized. |
| `value` | string | Created person UUID. |

## Native endpoint

Through the native OfficeMaps API, this operation is `POST /v1/person` (base URL `https://api.officemaps.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person.md) for the provider-specific parameters and requirements.

