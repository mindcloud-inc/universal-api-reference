# ServerAvatar: Get Organization

Retrieves an organization from ServerAvatar.

```
GET https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServerAvatar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-organization?connectionId=$CONNECTION_ID&organization=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-organization?${params}`, {
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
| `organization` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "organization": {
        "admin": true,
        "createdAt": "string",
        "deletedAt": "string",
        "description": "string",
        "id": 1,
        "logo": "string",
        "main": 1,
        "name": "Ava Chen",
        "updatedAt": "string",
        "user": {
          "avatar": "string",
          "companySize": "string",
          "confirmationTimer": 1,
          "countryCode": "string",
          "countryName": "Ava Chen",
          "createdAt": "string",
          "credits": 1,
          "defaultPlan": "string",
          "deletedAt": "string",
          "deleteProtection": true,
          "email": "ava@example.com",
          "emailVerifiedAt": "ava@example.com",
          "freeCredits": 1,
          "google2faEnable": true,
          "heardAboutUs": "string",
          "id": 1,
          "industry": "string",
          "isCloudHosting": 1,
          "isOnboarding": true,
          "managementExperience": "string",
          "mobileNo": "string",
          "name": "Ava Chen",
          "negativePeriod": 1,
          "newSubscriptionPlan": {
            "allowedApplications": 1,
            "allowedServers": 1,
            "createdAt": "string",
            "cycle": "string",
            "deletedAt": "string",
            "expiresInDays": 1,
            "id": 1,
            "name": "Ava Chen",
            "numberOfMonth": 1,
            "organizationId": 1,
            "pricePerMonth": 1,
            "type": "string",
            "updatedAt": "string",
            "userId": 1
          },
          "normalizedEmail": "ava@example.com",
          "pmLastFour": "string",
          "pmType": "string",
          "postpaid": 1,
          "rateLimit": "string",
          "receiveAccountUpdate": true,
          "receiveCredential": true,
          "receiveInformativeContent": true,
          "referralClicks": 1,
          "referralCode": "string",
          "regionCode": "string",
          "regionName": "Ava Chen",
          "reminderMinimumCredit": "string",
          "role": "string",
          "serverCredits": "string",
          "serverLimit": 1,
          "status": "string",
          "stripeId": "string",
          "timezone": "string",
          "toltReferral": "string",
          "twoFaEnable": true,
          "updatedAt": "string",
          "usesRestructuredTier": 1,
          "whitelistIp": true
        },
        "userId": 1,
        "uuid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organization` | object |  |
| `organization.admin` | boolean |  |
| `organization.createdAt` | string |  |
| `organization.deletedAt` | string |  |
| `organization.description` | string |  |
| `organization.id` | number |  |
| `organization.logo` | string |  |
| `organization.main` | number |  |
| `organization.name` | string |  |
| `organization.updatedAt` | string |  |
| `organization.user` | object |  |
| `organization.user.avatar` | string |  |
| `organization.user.companySize` | string |  |
| `organization.user.confirmationTimer` | number |  |
| `organization.user.countryCode` | string |  |
| `organization.user.countryName` | string |  |
| `organization.user.createdAt` | string |  |
| `organization.user.credits` | number |  |
| `organization.user.defaultPlan` | string |  |
| `organization.user.deletedAt` | string |  |
| `organization.user.deleteProtection` | boolean |  |
| `organization.user.email` | string |  |
| `organization.user.emailVerifiedAt` | string |  |
| `organization.user.freeCredits` | number |  |
| `organization.user.google2faEnable` | boolean |  |
| `organization.user.heardAboutUs` | string |  |
| `organization.user.id` | number |  |
| `organization.user.industry` | string |  |
| `organization.user.isCloudHosting` | number |  |
| `organization.user.isOnboarding` | boolean |  |
| `organization.user.managementExperience` | string |  |
| `organization.user.mobileNo` | string |  |
| `organization.user.name` | string |  |
| `organization.user.negativePeriod` | number |  |
| `organization.user.newSubscriptionPlan` | object |  |
| `organization.user.newSubscriptionPlan.allowedApplications` | number |  |
| `organization.user.newSubscriptionPlan.allowedServers` | number |  |
| `organization.user.newSubscriptionPlan.createdAt` | string |  |
| `organization.user.newSubscriptionPlan.cycle` | string |  |
| `organization.user.newSubscriptionPlan.deletedAt` | string |  |
| `organization.user.newSubscriptionPlan.expiresInDays` | number |  |
| `organization.user.newSubscriptionPlan.id` | number |  |
| `organization.user.newSubscriptionPlan.name` | string |  |
| `organization.user.newSubscriptionPlan.numberOfMonth` | number |  |
| `organization.user.newSubscriptionPlan.organizationId` | number |  |
| `organization.user.newSubscriptionPlan.pricePerMonth` | number |  |
| `organization.user.newSubscriptionPlan.type` | string |  |
| `organization.user.newSubscriptionPlan.updatedAt` | string |  |
| `organization.user.newSubscriptionPlan.userId` | number |  |
| `organization.user.normalizedEmail` | string |  |
| `organization.user.pmLastFour` | string |  |
| `organization.user.pmType` | string |  |
| `organization.user.postpaid` | number |  |
| `organization.user.rateLimit` | string |  |
| `organization.user.receiveAccountUpdate` | boolean |  |
| `organization.user.receiveCredential` | boolean |  |
| `organization.user.receiveInformativeContent` | boolean |  |
| `organization.user.referralClicks` | number |  |
| `organization.user.referralCode` | string |  |
| `organization.user.regionCode` | string |  |
| `organization.user.regionName` | string |  |
| `organization.user.reminderMinimumCredit` | string |  |
| `organization.user.role` | string |  |
| `organization.user.serverCredits` | string |  |
| `organization.user.serverLimit` | number |  |
| `organization.user.status` | string |  |
| `organization.user.stripeId` | string |  |
| `organization.user.timezone` | string |  |
| `organization.user.toltReferral` | string |  |
| `organization.user.twoFaEnable` | boolean |  |
| `organization.user.updatedAt` | string |  |
| `organization.user.usesRestructuredTier` | number |  |
| `organization.user.whitelistIp` | boolean |  |
| `organization.userId` | number |  |
| `organization.uuid` | string |  |

## Native endpoint

Through the native ServerAvatar API, this operation is `GET /organizations/{{organization}}` (base URL `https://api.serveravatar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

