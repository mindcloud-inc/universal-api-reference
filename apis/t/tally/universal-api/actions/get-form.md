# Tally: Get Form



```
GET https://connect.mindcloud.co/v1/universal/tally/latest/actions/get-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tally `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tally/latest/actions/get-form?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tally/latest/actions/get-form?${params}`, {
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
| `formId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blocks": [
        {
          "groupType": "string",
          "groupUuid": "string",
          "type": "string",
          "uuid": "string"
        }
      ],
      "createdAt": "string",
      "hasDraftBlocks": true,
      "id": "string",
      "index": 1,
      "isClosed": true,
      "isNameModifiedByUser": true,
      "name": "Ava Chen",
      "numberOfSubmissions": 1,
      "organizationId": "string",
      "settings": {
        "closeDate": {},
        "closeMessageDescription": {},
        "closeMessageTitle": {},
        "closeTime": {},
        "closeTimezone": {},
        "hasPartialSubmissions": true,
        "hasProgressBar": true,
        "hasRespondentEmailNotifications": true,
        "hasSelfEmailNotifications": true,
        "hasVerifyEmailNotifications": true,
        "isClosed": true,
        "language": "string",
        "metaDescription": {},
        "metaImageUrl": {},
        "metaSiteFaviconUrl": {},
        "metaSiteName": {},
        "metaTitle": {},
        "pageAutoJump": true,
        "password": {},
        "redirectOnCompletion": {},
        "respondentEmailBody": {},
        "respondentEmailFromName": {},
        "respondentEmailReplyTo": {},
        "respondentEmailSendingDomainId": {},
        "respondentEmailSubject": {},
        "respondentEmailTo": {},
        "saveForLater": true,
        "selfEmailBody": {},
        "selfEmailFromName": {},
        "selfEmailReplyTo": {},
        "selfEmailSendingDomainId": {},
        "selfEmailSubject": {},
        "selfEmailTo": {},
        "styles": {},
        "submissionsDataRetentionDuration": {},
        "submissionsDataRetentionUnit": {},
        "submissionsLimit": {},
        "uniqueSubmissionKey": {},
        "verifyEmailFromName": {},
        "verifyEmailSendingDomainId": {}
      },
      "status": "string",
      "updatedAt": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocks[].groupType` | string |  |
| `blocks[].groupUuid` | string |  |
| `blocks[].type` | string |  |
| `blocks[].uuid` | string |  |
| `createdAt` | string |  |
| `hasDraftBlocks` | boolean |  |
| `id` | string |  |
| `index` | number |  |
| `isClosed` | boolean |  |
| `isNameModifiedByUser` | boolean |  |
| `name` | string |  |
| `numberOfSubmissions` | number |  |
| `organizationId` | string |  |
| `settings.closeDate` | object |  |
| `settings.closeMessageDescription` | object |  |
| `settings.closeMessageTitle` | object |  |
| `settings.closeTime` | object |  |
| `settings.closeTimezone` | object |  |
| `settings.hasPartialSubmissions` | boolean |  |
| `settings.hasProgressBar` | boolean |  |
| `settings.hasRespondentEmailNotifications` | boolean |  |
| `settings.hasSelfEmailNotifications` | boolean |  |
| `settings.hasVerifyEmailNotifications` | boolean |  |
| `settings.isClosed` | boolean |  |
| `settings.language` | string |  |
| `settings.metaDescription` | object |  |
| `settings.metaImageUrl` | object |  |
| `settings.metaSiteFaviconUrl` | object |  |
| `settings.metaSiteName` | object |  |
| `settings.metaTitle` | object |  |
| `settings.pageAutoJump` | boolean |  |
| `settings.password` | object |  |
| `settings.redirectOnCompletion` | object |  |
| `settings.respondentEmailBody` | object |  |
| `settings.respondentEmailFromName` | object |  |
| `settings.respondentEmailReplyTo` | object |  |
| `settings.respondentEmailSendingDomainId` | object |  |
| `settings.respondentEmailSubject` | object |  |
| `settings.respondentEmailTo` | object |  |
| `settings.saveForLater` | boolean |  |
| `settings.selfEmailBody` | object |  |
| `settings.selfEmailFromName` | object |  |
| `settings.selfEmailReplyTo` | object |  |
| `settings.selfEmailSendingDomainId` | object |  |
| `settings.selfEmailSubject` | object |  |
| `settings.selfEmailTo` | object |  |
| `settings.styles` | object |  |
| `settings.submissionsDataRetentionDuration` | object |  |
| `settings.submissionsDataRetentionUnit` | object |  |
| `settings.submissionsLimit` | object |  |
| `settings.uniqueSubmissionKey` | object |  |
| `settings.verifyEmailFromName` | object |  |
| `settings.verifyEmailSendingDomainId` | object |  |
| `status` | string |  |
| `updatedAt` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Tally API, this operation is `GET forms/:formId` (base URL `https://api.tally.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form.md) for the provider-specific parameters and requirements.

