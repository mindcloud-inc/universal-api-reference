# lemlist: List Activities

Retrieves your activity records from lemlist.

```
GET https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/list-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lemlist `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/list-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/list-activities?${params}`, {
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
| `type` | string | no | Filter by activity type. Example: `paused`. |
| `campaignId` | string | no | Filter by campaign ID. Example: `cam_123`. |
| `isFirst` | boolean | no | Filter for first activity only. |
| `leadId` | string | no | Filter by lead ID. Example: `lea_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aiLeadInterestScore": 1,
      "bot": true,
      "bouncedId": "string",
      "campaignId": "string",
      "campaignName": "Ava Chen",
      "cc": [
        "string"
      ],
      "contactId": "string",
      "createdAt": "string",
      "createdBy": "string",
      "emailId": "ava@example.com",
      "fromEmail": "ava@example.com",
      "id": "string",
      "isFirst": true,
      "lead": {
        "contactId": "string",
        "enrichment": {},
        "id": "string",
        "isPaused": true,
        "personalized": true,
        "source": "string",
        "state": "string",
        "updatedAt": "string",
        "variables": {
          "companyDomain": "string",
          "companyLinkedinUrl": "https://example.com",
          "companyName": "Ava Chen",
          "email": "ava@example.com",
          "firstName": "Ava",
          "jobTitle": "string",
          "lastName": "Chen",
          "linkedinUrl": "https://example.com",
          "phone": "string",
          "preferredContactMethod": "string"
        }
      },
      "leadCompanyName": "Ava Chen",
      "leadEmail": "ava@example.com",
      "leadFirstName": "Ava",
      "leadId": "string",
      "leadLastName": "Chen",
      "leadPhone": "string",
      "messageId": "string",
      "messagePreview": "string",
      "metaData": {
        "campaignId": "string",
        "createdBy": "string",
        "leadId": "string",
        "s3ready": true,
        "taskId": "string",
        "teamId": "string",
        "type": "string"
      },
      "name": "Ava Chen",
      "sendUserEmail": "ava@example.com",
      "sendUserId": "string",
      "sendUserLoginEmail": "ava@example.com",
      "sendUserMailboxId": "string",
      "sendUserName": "Ava Chen",
      "sequenceTested": "string",
      "stopped": true,
      "subject": "string",
      "teamId": "string",
      "type": "string",
      "unsubscribedSource": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiLeadInterestScore` | number |  |
| `bot` | boolean |  |
| `bouncedId` | string |  |
| `campaignId` | string |  |
| `campaignName` | string |  |
| `cc` | array<string> |  |
| `contactId` | string |  |
| `createdAt` | string |  |
| `createdBy` | string |  |
| `emailId` | string |  |
| `fromEmail` | string |  |
| `id` | string |  |
| `isFirst` | boolean |  |
| `lead` | object |  |
| `lead.contactId` | string |  |
| `lead.enrichment` | object |  |
| `lead.id` | string |  |
| `lead.isPaused` | boolean |  |
| `lead.personalized` | boolean |  |
| `lead.source` | string |  |
| `lead.state` | string |  |
| `lead.updatedAt` | string |  |
| `lead.variables` | object |  |
| `lead.variables.companyDomain` | string |  |
| `lead.variables.companyLinkedinUrl` | string |  |
| `lead.variables.companyName` | string |  |
| `lead.variables.email` | string |  |
| `lead.variables.firstName` | string |  |
| `lead.variables.jobTitle` | string |  |
| `lead.variables.lastName` | string |  |
| `lead.variables.linkedinUrl` | string |  |
| `lead.variables.phone` | string |  |
| `lead.variables.preferredContactMethod` | string |  |
| `leadCompanyName` | string |  |
| `leadEmail` | string |  |
| `leadFirstName` | string |  |
| `leadId` | string |  |
| `leadLastName` | string |  |
| `leadPhone` | string |  |
| `messageId` | string |  |
| `messagePreview` | string |  |
| `metaData` | object |  |
| `metaData.campaignId` | string |  |
| `metaData.createdBy` | string |  |
| `metaData.leadId` | string |  |
| `metaData.s3ready` | boolean |  |
| `metaData.taskId` | string |  |
| `metaData.teamId` | string |  |
| `metaData.type` | string |  |
| `name` | string |  |
| `sendUserEmail` | string |  |
| `sendUserId` | string |  |
| `sendUserLoginEmail` | string |  |
| `sendUserMailboxId` | string |  |
| `sendUserName` | string |  |
| `sequenceTested` | string |  |
| `stopped` | boolean |  |
| `subject` | string |  |
| `teamId` | string |  |
| `type` | string |  |
| `unsubscribedSource` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native lemlist API, this operation is `GET /activities` (base URL `https://api.lemlist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-activities.md) for the provider-specific parameters and requirements.

