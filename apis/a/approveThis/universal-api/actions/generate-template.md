# ApproveThis: Generate Template

Creates an approval template from JSON data in ApproveThis.

```
POST https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/generate-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ApproveThis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/generate-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/generate-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | An object containing template, page, and fields definitions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true,
      "template": {
        "allowAnonymousResponses": true,
        "createdAt": "string",
        "description": "string",
        "id": 1,
        "isActive": true,
        "name": "Ava Chen",
        "ownerId": "string",
        "ownerType": "string",
        "pages": [
          {
            "address": "string",
            "confirmationPage": {},
            "content": {},
            "createdAt": "string",
            "deletedAt": {},
            "headline": "string",
            "id": 1,
            "name": "Ava Chen",
            "slug": "string",
            "teamId": 1,
            "template": {
              "actions": {},
              "allowAnonymousResponses": 1,
              "createdAt": "string",
              "deletedAt": {},
              "description": "string",
              "id": 1,
              "isActive": true,
              "isDemo": 1,
              "layouts": {},
              "name": "Ava Chen",
              "ownerId": "string",
              "ownerType": "string",
              "properties": {},
              "settings": {
                "allowResubmissions": true,
                "commentsEnabled": true,
                "commentsImmutable": true,
                "loginForApprovers": true,
                "maxResubmissions": {},
                "signedUrlExpirationDays": 1,
                "signedUrlsEnabled": true
              },
              "slug": "string",
              "teamId": 1,
              "type": "string",
              "updatedAt": "string"
            },
            "templateId": 1,
            "thankYou": {},
            "updatedAt": "string",
            "welcomePage": {}
          }
        ],
        "settings": {
          "allowResubmissions": true,
          "commentsEnabled": true,
          "commentsImmutable": true,
          "loginForApprovers": true,
          "maxResubmissions": {},
          "signedUrlExpirationDays": 1,
          "signedUrlsEnabled": true
        },
        "slug": "string",
        "team": {
          "approvalHubActive": true,
          "createdAt": "string",
          "deletedAt": {},
          "domain": "string",
          "domainVerifiedAt": {},
          "id": 1,
          "isDemo": 1,
          "licenseKeys": {},
          "licenseType": "string",
          "logoPath": {},
          "logoUrl": "https://example.com",
          "name": "Ava Chen",
          "owner": {
            "adminMode": 1,
            "avatar": "string",
            "createdAt": "string",
            "currentConnectedAccountId": {},
            "currentTeamId": "string",
            "deletedAt": {},
            "email": "ava@example.com",
            "emailVerifiedAt": {},
            "firstName": "Ava",
            "id": "string",
            "isDemo": 1,
            "lastName": "Chen",
            "marketingUnsubscribed": 1,
            "marketingUnsubscribedAt": {},
            "name": "Ava Chen",
            "phone": {},
            "phoneCountry": {},
            "phoneVerifiedAt": {},
            "profilePhotoPath": {},
            "timezone": "string",
            "title": {},
            "twoFactorConfirmedAt": {},
            "type": "string",
            "unregisteredUser": true,
            "updatedAt": "string"
          },
          "personalTeam": true,
          "stripeSubscription": {
            "billingInterval": "string",
            "createdAt": "string",
            "endsAt": {},
            "id": 1,
            "paymentFailedAt": {},
            "planId": "string",
            "stripeCustomerId": "string",
            "stripeStatus": "string",
            "stripeSubscriptionId": "string",
            "teamId": 1,
            "trialEndsAt": "string",
            "updatedAt": "string",
            "workflowPacks": 1,
            "workflowTier": 1
          },
          "subdomain": "string",
          "updatedAt": "string",
          "userId": "string"
        },
        "teamId": 1,
        "type": "string",
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `success` | boolean |  |
| `template.allowAnonymousResponses` | boolean |  |
| `template.createdAt` | string |  |
| `template.description` | string |  |
| `template.id` | number |  |
| `template.isActive` | boolean |  |
| `template.name` | string |  |
| `template.ownerId` | string |  |
| `template.ownerType` | string |  |
| `template.pages[].address` | string |  |
| `template.pages[].confirmationPage` | object |  |
| `template.pages[].content` | object |  |
| `template.pages[].createdAt` | string |  |
| `template.pages[].deletedAt` | object |  |
| `template.pages[].headline` | string |  |
| `template.pages[].id` | number |  |
| `template.pages[].name` | string |  |
| `template.pages[].slug` | string |  |
| `template.pages[].teamId` | number |  |
| `template.pages[].template.actions` | object |  |
| `template.pages[].template.allowAnonymousResponses` | number |  |
| `template.pages[].template.createdAt` | string |  |
| `template.pages[].template.deletedAt` | object |  |
| `template.pages[].template.description` | string |  |
| `template.pages[].template.id` | number |  |
| `template.pages[].template.isActive` | boolean |  |
| `template.pages[].template.isDemo` | number |  |
| `template.pages[].template.layouts` | object |  |
| `template.pages[].template.name` | string |  |
| `template.pages[].template.ownerId` | string |  |
| `template.pages[].template.ownerType` | string |  |
| `template.pages[].template.properties` | object |  |
| `template.pages[].template.settings.allowResubmissions` | boolean |  |
| `template.pages[].template.settings.commentsEnabled` | boolean |  |
| `template.pages[].template.settings.commentsImmutable` | boolean |  |
| `template.pages[].template.settings.loginForApprovers` | boolean |  |
| `template.pages[].template.settings.maxResubmissions` | object |  |
| `template.pages[].template.settings.signedUrlExpirationDays` | number |  |
| `template.pages[].template.settings.signedUrlsEnabled` | boolean |  |
| `template.pages[].template.slug` | string |  |
| `template.pages[].template.teamId` | number |  |
| `template.pages[].template.type` | string |  |
| `template.pages[].template.updatedAt` | string |  |
| `template.pages[].templateId` | number |  |
| `template.pages[].thankYou` | object |  |
| `template.pages[].updatedAt` | string |  |
| `template.pages[].welcomePage` | object |  |
| `template.settings.allowResubmissions` | boolean |  |
| `template.settings.commentsEnabled` | boolean |  |
| `template.settings.commentsImmutable` | boolean |  |
| `template.settings.loginForApprovers` | boolean |  |
| `template.settings.maxResubmissions` | object |  |
| `template.settings.signedUrlExpirationDays` | number |  |
| `template.settings.signedUrlsEnabled` | boolean |  |
| `template.slug` | string |  |
| `template.team.approvalHubActive` | boolean |  |
| `template.team.createdAt` | string |  |
| `template.team.deletedAt` | object |  |
| `template.team.domain` | string |  |
| `template.team.domainVerifiedAt` | object |  |
| `template.team.id` | number |  |
| `template.team.isDemo` | number |  |
| `template.team.licenseKeys` | object |  |
| `template.team.licenseType` | string |  |
| `template.team.logoPath` | object |  |
| `template.team.logoUrl` | string |  |
| `template.team.name` | string |  |
| `template.team.owner.adminMode` | number |  |
| `template.team.owner.avatar` | string |  |
| `template.team.owner.createdAt` | string |  |
| `template.team.owner.currentConnectedAccountId` | object |  |
| `template.team.owner.currentTeamId` | string |  |
| `template.team.owner.deletedAt` | object |  |
| `template.team.owner.email` | string |  |
| `template.team.owner.emailVerifiedAt` | object |  |
| `template.team.owner.firstName` | string |  |
| `template.team.owner.id` | string |  |
| `template.team.owner.isDemo` | number |  |
| `template.team.owner.lastName` | string |  |
| `template.team.owner.marketingUnsubscribed` | number |  |
| `template.team.owner.marketingUnsubscribedAt` | object |  |
| `template.team.owner.name` | string |  |
| `template.team.owner.phone` | object |  |
| `template.team.owner.phoneCountry` | object |  |
| `template.team.owner.phoneVerifiedAt` | object |  |
| `template.team.owner.profilePhotoPath` | object |  |
| `template.team.owner.timezone` | string |  |
| `template.team.owner.title` | object |  |
| `template.team.owner.twoFactorConfirmedAt` | object |  |
| `template.team.owner.type` | string |  |
| `template.team.owner.unregisteredUser` | boolean |  |
| `template.team.owner.updatedAt` | string |  |
| `template.team.personalTeam` | boolean |  |
| `template.team.stripeSubscription.billingInterval` | string |  |
| `template.team.stripeSubscription.createdAt` | string |  |
| `template.team.stripeSubscription.endsAt` | object |  |
| `template.team.stripeSubscription.id` | number |  |
| `template.team.stripeSubscription.paymentFailedAt` | object |  |
| `template.team.stripeSubscription.planId` | string |  |
| `template.team.stripeSubscription.stripeCustomerId` | string |  |
| `template.team.stripeSubscription.stripeStatus` | string |  |
| `template.team.stripeSubscription.stripeSubscriptionId` | string |  |
| `template.team.stripeSubscription.teamId` | number |  |
| `template.team.stripeSubscription.trialEndsAt` | string |  |
| `template.team.stripeSubscription.updatedAt` | string |  |
| `template.team.stripeSubscription.workflowPacks` | number |  |
| `template.team.stripeSubscription.workflowTier` | number |  |
| `template.team.subdomain` | string |  |
| `template.team.updatedAt` | string |  |
| `template.team.userId` | string |  |
| `template.teamId` | number |  |
| `template.type` | string |  |
| `template.updatedAt` | string |  |

## Native endpoint

Through the native ApproveThis API, this operation is `POST /templates/generate` (base URL `https://app.approvethis.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-template.md) for the provider-specific parameters and requirements.

