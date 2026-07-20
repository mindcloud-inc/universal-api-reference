# Rossum: List Users

Retrieves users from Rossum.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-users?${params}`, {
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
| `email` | string | no | Filter users by email address. |
| `ordering` | string | no | Ordering expression, for example email or -email. |
| `organization` | string | no | Filter users by Rossum organization URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "next": {},
        "previous": {}
      },
      "results": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.next` | object |  |
| `pagination.previous` | object |  |
| `results[].authType` | string |  |
| `results[].dateJoined` | string |  |
| `results[].deleted` | boolean |  |
| `results[].email` | string |  |
| `results[].emailVerified` | boolean |  |
| `results[].firstName` | string |  |
| `results[].groups[]` | string |  |
| `results[].id` | number |  |
| `results[].isActive` | boolean |  |
| `results[].lastLogin` | string |  |
| `results[].lastName` | string |  |
| `results[].oidcId` | object |  |
| `results[].organization` | string |  |
| `results[].phoneNumber` | string |  |
| `results[].uiSettings.complexLineItems` | boolean |  |
| `results[].uiSettings.dashboard.workspacesSorting` | string |  |
| `results[].uiSettings.isUsingNewDashboard` | boolean |  |
| `results[].uiSettings.locale` | string |  |
| `results[].uiSettings.onboardingAcknowledged` | boolean |  |
| `results[].uiSettings.onboardingSurvey.activeStep` | string |  |
| `results[].uiSettings.onboardingSurvey.stepsData.whatIsYourRole.selectedOptions[]` | string |  |
| `results[].uiSettings.showConfidenceScore` | boolean |  |
| `results[].url` | string |  |
| `results[].username` | string |  |

## Native endpoint

Through the native Rossum API, this operation is `GET /users` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

