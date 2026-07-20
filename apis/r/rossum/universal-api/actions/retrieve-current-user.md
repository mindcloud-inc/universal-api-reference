# Rossum: Retrieve Current User

Retrieves the current user from Rossum.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-current-user?${params}`, {
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
      "authType": "string",
      "dateJoined": "string",
      "deleted": true,
      "email": "ava@example.com",
      "emailVerified": true,
      "firstName": "Ava",
      "groups": [
        "string"
      ],
      "id": 1,
      "isActive": true,
      "lastLogin": "string",
      "lastName": "Chen",
      "oidcId": {},
      "organization": "string",
      "phoneNumber": "string",
      "uiSettings": {
        "complexLineItems": true,
        "dashboard": {
          "workspacesSorting": "string"
        },
        "isUsingNewDashboard": true,
        "locale": "string",
        "onboardingAcknowledged": true,
        "onboardingSurvey": {
          "activeStep": "string",
          "stepsData": {
            "whatIsYourRole": {
              "selectedOptions": [
                "string"
              ]
            }
          }
        },
        "showConfidenceScore": true
      },
      "url": "https://example.com",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authType` | string |  |
| `dateJoined` | string |  |
| `deleted` | boolean |  |
| `email` | string |  |
| `emailVerified` | boolean |  |
| `firstName` | string |  |
| `groups[]` | string |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `lastLogin` | string |  |
| `lastName` | string |  |
| `oidcId` | object |  |
| `organization` | string |  |
| `phoneNumber` | string |  |
| `uiSettings.complexLineItems` | boolean |  |
| `uiSettings.dashboard.workspacesSorting` | string |  |
| `uiSettings.isUsingNewDashboard` | boolean |  |
| `uiSettings.locale` | string |  |
| `uiSettings.onboardingAcknowledged` | boolean |  |
| `uiSettings.onboardingSurvey.activeStep` | string |  |
| `uiSettings.onboardingSurvey.stepsData.whatIsYourRole.selectedOptions[]` | string |  |
| `uiSettings.showConfidenceScore` | boolean |  |
| `url` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Rossum API, this operation is `GET /auth/user` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-current-user.md) for the provider-specific parameters and requirements.

