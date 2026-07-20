# Apollo: Bulk Create Contacts

Creates multiple new contacts in Apollo.

```
POST https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/bulk-create-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/bulk-create-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/bulk-create-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contacts[]` | array<object> | yes | Array of contact objects to create (maximum 100 contacts per request) |
| `contacts[].firstName` | string | no | Contact's first name |
| `contacts[].lastName` | string | no | Contact's last name |
| `contacts[].email` | string | no | Contact's email address |
| `contacts[].title` | string | no | Contact's job title |
| `contacts[].primaryTitle` | string | no | Primary job title (takes precedence over title) |
| `contacts[].organizationName` | string | no | Company/organization name |
| `contacts[].phone` | string | no | Phone number |
| `contacts[].presentRawAddress` | string | no | Physical address |
| `contacts[].linkedinUrl` | string | no | LinkedIn profile URL |
| `contacts[].facebookUrl` | string | no | Facebook profile URL |
| `contacts[].twitterUrl` | string | no | Twitter profile URL |
| `contacts[].photoUrl` | string | no | Profile photo URL |
| `contacts[].accountId` | string | no | Associated account ID |
| `contacts[].organizationId` | string | no | Associated organization ID |
| `contacts[].ownerId` | string | no | Contact owner user ID (defaults to current user if not provided) |
| `contacts[].contactStageId` | string | no | Contact stage ID |
| `contacts[].salesforceId` | string | no | Salesforce ID for matching and deduplication |
| `contacts[].hubspotId` | string | no | HubSpot ID for matching and deduplication |
| `contacts[].salesforceLeadId` | string | no | Salesforce Lead ID |
| `contacts[].salesforceContactId` | string | no | Salesforce Contact ID for matching |
| `contacts[].salesforceAccountId` | string | no | Salesforce Account ID |
| `contacts[].outreachId` | string | no | Outreach.io ID |
| `contacts[].salesloftId` | string | no | SalesLoft ID |
| `contacts[].phoneStatusCd` | string | no | Phone validation status |
| `contacts[].typedCustomFields` | object | no | Custom field values as key-value pairs where key is the field_id and value is the field_value |
| `contacts[].contactEmails[]` | array<object> | no | Array of email objects with position |
| `contacts[].contactEmails[].email` | string | no |  |
| `contacts[].contactEmails[].position` | number | no |  |
| `contacts[].phoneNumbers[]` | array<object> | no | Array of phone number objects |
| `contacts[].phoneNumbers[].rawNumber` | string | no |  |
| `contacts[].phoneNumbers[].position` | number | no |  |
| `contacts[].contactRoleTypeIds[]` | array<string> | no | Array of contact role type IDs |
| `contacts[].appendLabelNames[]` | array<string> | no | Array of label names to add to the contact |
| `runDedupe` | boolean | no | Enable full deduplication across all sources. When false (default), creates duplicates for non-email_import sources and merges with email_import placeholders only. When true, returns existing contacts without modifying them (except email_import placeholders which are still merged). Matches by email, CRM IDs, or name + organization |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdContacts": [
        {
          "accountId": {},
          "accountPhoneNote": {},
          "callOptedOut": {},
          "city": {},
          "contactEmails": [
            {
              "email": "ava@example.com",
              "emailMd5": "ava@example.com",
              "emailNeedsTickling": true,
              "emailSha256": "ava@example.com",
              "emailStatus": "ava@example.com",
              "emailStatusUnavailableReason": {},
              "emailTrueStatus": "ava@example.com",
              "extrapolatedEmailConfidence": {},
              "freeDomain": true,
              "position": 1,
              "source": "ava@example.com",
              "thirdPartyVendorName": {}
            }
          ],
          "contactStageId": "string",
          "country": {},
          "createdAt": "2026-05-07T12:00:00.000Z",
          "creatorId": "string",
          "crmId": {},
          "crmOwnerId": {},
          "crmRecordUrl": {},
          "customFieldErrors": {},
          "directDialEnrichmentFailedAt": {},
          "directDialStatus": {},
          "email": "ava@example.com",
          "emailDomainCatchall": true,
          "emailFromCustomer": true,
          "emailNeedsTickling": true,
          "emailSource": {},
          "emailStatus": "ava@example.com",
          "emailStatusUnavailableReason": {},
          "emailTrueStatus": "ava@example.com",
          "emailUnsubscribed": {},
          "existenceLevel": "string",
          "extrapolatedEmailConfidence": {},
          "facebookUrl": {},
          "firstName": "Ava",
          "formattedAddress": {},
          "freeDomain": true,
          "hasEmailArcgateRequest": true,
          "hasPendingEmailArcgateRequest": true,
          "headline": {},
          "hubspotCompanyId": {},
          "hubspotVid": {},
          "id": "string",
          "intentStrength": {},
          "lastActivityDate": {},
          "lastName": "Chen",
          "linkedinUid": {},
          "linkedinUrl": {},
          "mergedCrmIds": {},
          "name": "Ava Chen",
          "organizationId": "string",
          "organizationName": "Ava Chen",
          "originalSource": "string",
          "ownerId": "string",
          "personDeleted": {},
          "personId": {},
          "photoUrl": {},
          "postalCode": {},
          "presentRawAddress": {},
          "queuedForCrmPush": {},
          "salesforceAccountId": {},
          "salesforceContactId": {},
          "salesforceId": {},
          "salesforceLeadId": {},
          "sanitizedPhone": {},
          "showIntent": true,
          "source": "string",
          "sourceDisplayName": "Ava Chen",
          "state": {},
          "streetAddress": {},
          "suggestedFromRuleEngineConfigId": {},
          "timeZone": {},
          "title": "string",
          "twitterUrl": {},
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "updatedEmailTrueStatus": true
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
| `createdContacts[].accountId` | object |  |
| `createdContacts[].accountPhoneNote` | object |  |
| `createdContacts[].callOptedOut` | object |  |
| `createdContacts[].city` | object |  |
| `createdContacts[].contactEmails[].email` | string |  |
| `createdContacts[].contactEmails[].emailMd5` | string |  |
| `createdContacts[].contactEmails[].emailNeedsTickling` | boolean |  |
| `createdContacts[].contactEmails[].emailSha256` | string |  |
| `createdContacts[].contactEmails[].emailStatus` | string |  |
| `createdContacts[].contactEmails[].emailStatusUnavailableReason` | object |  |
| `createdContacts[].contactEmails[].emailTrueStatus` | string |  |
| `createdContacts[].contactEmails[].extrapolatedEmailConfidence` | object |  |
| `createdContacts[].contactEmails[].freeDomain` | boolean |  |
| `createdContacts[].contactEmails[].position` | number |  |
| `createdContacts[].contactEmails[].source` | string |  |
| `createdContacts[].contactEmails[].thirdPartyVendorName` | object |  |
| `createdContacts[].contactStageId` | string |  |
| `createdContacts[].country` | object |  |
| `createdContacts[].createdAt` | date |  |
| `createdContacts[].creatorId` | string |  |
| `createdContacts[].crmId` | object |  |
| `createdContacts[].crmOwnerId` | object |  |
| `createdContacts[].crmRecordUrl` | object |  |
| `createdContacts[].customFieldErrors` | object |  |
| `createdContacts[].directDialEnrichmentFailedAt` | object |  |
| `createdContacts[].directDialStatus` | object |  |
| `createdContacts[].email` | string |  |
| `createdContacts[].emailDomainCatchall` | boolean |  |
| `createdContacts[].emailFromCustomer` | boolean |  |
| `createdContacts[].emailNeedsTickling` | boolean |  |
| `createdContacts[].emailSource` | object |  |
| `createdContacts[].emailStatus` | string |  |
| `createdContacts[].emailStatusUnavailableReason` | object |  |
| `createdContacts[].emailTrueStatus` | string |  |
| `createdContacts[].emailUnsubscribed` | object |  |
| `createdContacts[].existenceLevel` | string |  |
| `createdContacts[].extrapolatedEmailConfidence` | object |  |
| `createdContacts[].facebookUrl` | object |  |
| `createdContacts[].firstName` | string |  |
| `createdContacts[].formattedAddress` | object |  |
| `createdContacts[].freeDomain` | boolean |  |
| `createdContacts[].hasEmailArcgateRequest` | boolean |  |
| `createdContacts[].hasPendingEmailArcgateRequest` | boolean |  |
| `createdContacts[].headline` | object |  |
| `createdContacts[].hubspotCompanyId` | object |  |
| `createdContacts[].hubspotVid` | object |  |
| `createdContacts[].id` | string |  |
| `createdContacts[].intentStrength` | object |  |
| `createdContacts[].lastActivityDate` | object |  |
| `createdContacts[].lastName` | string |  |
| `createdContacts[].linkedinUid` | object |  |
| `createdContacts[].linkedinUrl` | object |  |
| `createdContacts[].mergedCrmIds` | object |  |
| `createdContacts[].name` | string |  |
| `createdContacts[].organizationId` | string |  |
| `createdContacts[].organizationName` | string |  |
| `createdContacts[].originalSource` | string |  |
| `createdContacts[].ownerId` | string |  |
| `createdContacts[].personDeleted` | object |  |
| `createdContacts[].personId` | object |  |
| `createdContacts[].photoUrl` | object |  |
| `createdContacts[].postalCode` | object |  |
| `createdContacts[].presentRawAddress` | object |  |
| `createdContacts[].queuedForCrmPush` | object |  |
| `createdContacts[].salesforceAccountId` | object |  |
| `createdContacts[].salesforceContactId` | object |  |
| `createdContacts[].salesforceId` | object |  |
| `createdContacts[].salesforceLeadId` | object |  |
| `createdContacts[].sanitizedPhone` | object |  |
| `createdContacts[].showIntent` | boolean |  |
| `createdContacts[].source` | string |  |
| `createdContacts[].sourceDisplayName` | string |  |
| `createdContacts[].state` | object |  |
| `createdContacts[].streetAddress` | object |  |
| `createdContacts[].suggestedFromRuleEngineConfigId` | object |  |
| `createdContacts[].timeZone` | object |  |
| `createdContacts[].title` | string |  |
| `createdContacts[].twitterUrl` | object |  |
| `createdContacts[].updatedAt` | date |  |
| `createdContacts[].updatedEmailTrueStatus` | boolean |  |

## Native endpoint

Through the native Apollo API, this operation is `POST v1/contacts/bulk_create` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-create-contacts.md) for the provider-specific parameters and requirements.

