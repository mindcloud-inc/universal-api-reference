# Moxie: List Workspace Users

Retrieves workspace users from Moxie.

```
GET https://connect.mindcloud.co/v1/universal/moxie/latest/actions/list-workspace-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moxie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/list-workspace-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moxie/latest/actions/list-workspace-users?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "user": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "phoneVerified": true,
        "pricingVersion": 1,
        "uploadedPicture": true,
        "userAccounts": [
          {
            "account": {
              "accountId": 1,
              "accountName": "Ava Chen",
              "disabled": true,
              "free": true,
              "inTrial": true,
              "ltd": true,
              "paid": true,
              "pod": {
                "podId": "string",
                "podUrl": "https://example.com"
              },
              "pricingVersion": 1,
              "restricted": true,
              "sampleMode": true,
              "starter": true,
              "subscriptionProvider": "string",
              "subscriptionState": "string",
              "subscriptionType": "string",
              "trialEndsAt": "2026-05-07T12:00:00.000Z"
            },
            "userType": "string"
          }
        ],
        "userId": 1,
        "uuid": "string"
      },
      "userType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `user.email` | string |  |
| `user.firstName` | string |  |
| `user.lastName` | string |  |
| `user.phoneVerified` | boolean |  |
| `user.pricingVersion` | number |  |
| `user.uploadedPicture` | boolean |  |
| `user.userAccounts[].account.accountId` | number |  |
| `user.userAccounts[].account.accountName` | string |  |
| `user.userAccounts[].account.disabled` | boolean |  |
| `user.userAccounts[].account.free` | boolean |  |
| `user.userAccounts[].account.inTrial` | boolean |  |
| `user.userAccounts[].account.ltd` | boolean |  |
| `user.userAccounts[].account.paid` | boolean |  |
| `user.userAccounts[].account.pod.podId` | string |  |
| `user.userAccounts[].account.pod.podUrl` | string |  |
| `user.userAccounts[].account.pricingVersion` | number |  |
| `user.userAccounts[].account.restricted` | boolean |  |
| `user.userAccounts[].account.sampleMode` | boolean |  |
| `user.userAccounts[].account.starter` | boolean |  |
| `user.userAccounts[].account.subscriptionProvider` | string |  |
| `user.userAccounts[].account.subscriptionState` | string |  |
| `user.userAccounts[].account.subscriptionType` | string |  |
| `user.userAccounts[].account.trialEndsAt` | date |  |
| `user.userAccounts[].userType` | string |  |
| `user.userId` | number |  |
| `user.uuid` | string |  |
| `userType` | string |  |

## Native endpoint

Through the native Moxie API, this operation is `GET /action/users/list` (base URL `https://pod01.withmoxie.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-users.md) for the provider-specific parameters and requirements.

