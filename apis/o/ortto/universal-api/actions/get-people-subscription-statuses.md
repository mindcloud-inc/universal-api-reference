# Ortto: Get People Subscription Statuses



```
GET https://connect.mindcloud.co/v1/universal/ortto/latest/actions/get-people-subscription-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ortto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/get-people-subscription-statuses?connectionId=$CONNECTION_ID&people%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "people[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ortto/latest/actions/get-people-subscription-statuses?${params}`, {
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
| `people[]` | array<object> | yes | People to check subscription statuses for. Each item can include email or person_id. |
| `audienceId` | string | no | Specific audience ID to check when retrieving audience subscription status. |
| `subscription` | string | no | Subscription type to inspect, such as email or sms. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "people": [
        {
          "androidPermissions": true,
          "emailPermissions": true,
          "iosPermissions": true,
          "personId": "string",
          "personStatus": "string",
          "smsPermissions": true,
          "subscriptions": [
            {
              "androidOptedIn": true,
              "audienceId": "string",
              "audienceName": "Ava Chen",
              "iosOptedIn": true,
              "memberFrom": "string",
              "smsOptedIn": true,
              "subscribed": true,
              "subscribedFrom": "string",
              "webOptedIn": true,
              "whatsappOptedIn": true
            }
          ],
          "webPermissions": true
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `people[].androidPermissions` | boolean |  |
| `people[].emailPermissions` | boolean |  |
| `people[].iosPermissions` | boolean |  |
| `people[].personId` | string |  |
| `people[].personStatus` | string |  |
| `people[].smsPermissions` | boolean |  |
| `people[].subscriptions[].androidOptedIn` | boolean |  |
| `people[].subscriptions[].audienceId` | string |  |
| `people[].subscriptions[].audienceName` | string |  |
| `people[].subscriptions[].iosOptedIn` | boolean |  |
| `people[].subscriptions[].memberFrom` | string |  |
| `people[].subscriptions[].smsOptedIn` | boolean |  |
| `people[].subscriptions[].subscribed` | boolean |  |
| `people[].subscriptions[].subscribedFrom` | string |  |
| `people[].subscriptions[].webOptedIn` | boolean |  |
| `people[].subscriptions[].whatsappOptedIn` | boolean |  |
| `people[].webPermissions` | boolean |  |

## Native endpoint

Through the native Ortto API, this operation is `POST /person/subscriptions` (base URL `{{credentials.apiBaseUrl}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-people-subscription-statuses.md) for the provider-specific parameters and requirements.

