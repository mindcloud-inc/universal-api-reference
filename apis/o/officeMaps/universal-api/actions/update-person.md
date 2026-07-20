# OfficeMaps: Update Person

Updates an existing person in OfficeMaps.

```
PUT https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/update-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeMaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/update-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/update-person', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `badgeNumber` | string | no | Badge number. |
| `calendarViewId` | number | no | OfficeMaps calendar view ID. |
| `cell` | string | no | Person mobile number. |
| `directReports[]` | array<string> | no | List of direct report person IDs. |
| `displayName` | string | no | Preferred display name. |
| `email` | string | no | Person email address. |
| `employeeId` | string | no | External employee ID. |
| `facebookProfile` | string | no | Facebook profile URL. |
| `firstName` | string | no | Person first name. |
| `id` | string | yes | Person UUID. |
| `initials` | string | no | Person initials. |
| `isAllowOTPLogin` | boolean | no | Allow one-time-password login. |
| `isExcludeFromStatusNotifications` | boolean | no | Exclude from status notifications. |
| `isHiddenFromUsers` | boolean | no | Hide the person from users. |
| `lastName` | string | no | Person last name. |
| `linkedInProfile` | string | no | LinkedIn profile URL. |
| `personStatusComment` | string | no | Temporary status comment. |
| `personStatusExpiry` | date | no | Status expiry timestamp. |
| `personTypeId` | number | no | OfficeMaps person type ID. |
| `phone` | string | no | Person phone number. |
| `phoneExtension` | string | no | Person phone extension. |
| `position` | string | no | Person position or role. |
| `profileBlurb` | string | no | Profile blurb. |
| `reportsTo[]` | array<string> | no | List of manager person IDs. |
| `skypeName` | string | no | Skype name. |
| `title` | string | no | Person title. |
| `twitterProfile` | string | no | Twitter profile URL. |
| `username` | string | no | Person user name. |
| `webPage` | string | no | Personal or company web page. |

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
      "value": [
        "string"
      ]
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
| `value` | array<string> | Updated fields returned by OfficeMaps. |

## Native endpoint

Through the native OfficeMaps API, this operation is `PUT /v1/person/:id` (base URL `https://api.officemaps.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-person.md) for the provider-specific parameters and requirements.

