# Apollo: Create a Contact

Creates a new contact in Apollo.

```
POST https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/create-a-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/create-a-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/create-a-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | no | The first name of the contact you want to create. Example: `Tim` |
| `lastName` | string | no | The last name of the contact you want to create. Example: `Zheng` |
| `organizationName` | string | no | The name of the contact's employer (company). Example: `apollo` |
| `title` | string | no | The current job title that the contact holds. Example: `senior research analyst` |
| `accountId` | string | no | The Apollo ID for the account. Example: `63f53afe4ceeca00016bdd2f` |
| `email` | string | no | The email address of the contact. Example: `example@email.com` |
| `websiteUrl` | string | no | The corporate website URL. Example: `https://www.apollo.io/` |
| `labelNames[]` | array<string> | no | Lists to which the contact belongs. |
| `contactStageId` | string | no | The Apollo ID for the contact stage. Example: `6095a710bd01d100a506d4ae` |
| `presentRawAddress` | string | no | The personal location for the contact. Example: `Atlanta, United States` |
| `directPhone` | string | no | The primary phone number. Example: `555-303-1234` |
| `corporatePhone` | string | no | The work/office phone number. Example: `+44 7911 123456` |
| `mobilePhone` | string | no | The mobile phone number. Example: `555-303-1234` |
| `homePhone` | string | no | The home phone number. Example: `555-303-1234` |
| `otherPhone` | string | no | Alternative phone number. Example: `555-303-1234` |
| `typedCustomFields` | object | no | Add information to custom fields in Apollo. Your custom fields are unique to your team's Apollo account. This means that the examples in this documentation may not work for your testing purposes. To utilize this parameter successfully, call the Get a List of All Custom Fields endpoint and identify the `id` value for the custom field, as well as the appropriate data type. For example, if a custom field accepts picklist entries, you need to pass the accompanying `id` value for the picklist entry that you want to use as the input value. Example : When the Get a List of All Custom Fields endpoint returns an `id` of field: * `"60c39ed82bd02f01154c470a"` (datetime) then the value passed should be: `{"60c39ed82bd02f01154c470a": "2025-08-07"}` |
| `runDedupe` | boolean | no | Set to `true` to enable deduplication logic that prevents creating duplicate contacts. When enabled, Apollo will check for existing contacts with matching email addresses, names, or other identifying information and return the existing contact instead of creating a duplicate. The default value is `false`. When deduplication is enabled, performance may be slightly impacted due to the additional validation checks, but this ensures data integrity and prevents duplicate entries in your database. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "accountId": "string",
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
        "lastActivityDate": "2026-05-07T12:00:00.000Z",
        "lastName": "Chen",
        "linkedinUid": {},
        "linkedinUrl": {},
        "mergedCrmIds": {},
        "name": "Ava Chen",
        "nextContactId": {},
        "organizationId": "string",
        "organizationName": "Ava Chen",
        "originalSource": "string",
        "ownerId": "string",
        "personDeleted": {},
        "personId": {},
        "photoUrl": {},
        "postalCode": {},
        "presentRawAddress": {},
        "queuedForCrmPush": true,
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact.accountId` | string |  |
| `contact.accountPhoneNote` | object |  |
| `contact.callOptedOut` | object |  |
| `contact.city` | object |  |
| `contact.contactEmails[].email` | string |  |
| `contact.contactEmails[].emailMd5` | string |  |
| `contact.contactEmails[].emailNeedsTickling` | boolean |  |
| `contact.contactEmails[].emailSha256` | string |  |
| `contact.contactEmails[].emailStatus` | string |  |
| `contact.contactEmails[].emailStatusUnavailableReason` | object |  |
| `contact.contactEmails[].emailTrueStatus` | string |  |
| `contact.contactEmails[].extrapolatedEmailConfidence` | object |  |
| `contact.contactEmails[].freeDomain` | boolean |  |
| `contact.contactEmails[].position` | number |  |
| `contact.contactEmails[].source` | string |  |
| `contact.contactEmails[].thirdPartyVendorName` | object |  |
| `contact.contactStageId` | string |  |
| `contact.country` | object |  |
| `contact.createdAt` | date |  |
| `contact.creatorId` | string |  |
| `contact.crmId` | object |  |
| `contact.crmOwnerId` | object |  |
| `contact.crmRecordUrl` | object |  |
| `contact.directDialEnrichmentFailedAt` | object |  |
| `contact.directDialStatus` | object |  |
| `contact.email` | string |  |
| `contact.emailDomainCatchall` | boolean |  |
| `contact.emailFromCustomer` | boolean |  |
| `contact.emailNeedsTickling` | boolean |  |
| `contact.emailSource` | object |  |
| `contact.emailStatus` | string |  |
| `contact.emailStatusUnavailableReason` | object |  |
| `contact.emailTrueStatus` | string |  |
| `contact.emailUnsubscribed` | object |  |
| `contact.existenceLevel` | string |  |
| `contact.extrapolatedEmailConfidence` | object |  |
| `contact.facebookUrl` | object |  |
| `contact.firstName` | string |  |
| `contact.formattedAddress` | object |  |
| `contact.freeDomain` | boolean |  |
| `contact.hasEmailArcgateRequest` | boolean |  |
| `contact.hasPendingEmailArcgateRequest` | boolean |  |
| `contact.headline` | object |  |
| `contact.hubspotCompanyId` | object |  |
| `contact.hubspotVid` | object |  |
| `contact.id` | string |  |
| `contact.intentStrength` | object |  |
| `contact.lastActivityDate` | date |  |
| `contact.lastName` | string |  |
| `contact.linkedinUid` | object |  |
| `contact.linkedinUrl` | object |  |
| `contact.mergedCrmIds` | object |  |
| `contact.name` | string |  |
| `contact.nextContactId` | object |  |
| `contact.organizationId` | string |  |
| `contact.organizationName` | string |  |
| `contact.originalSource` | string |  |
| `contact.ownerId` | string |  |
| `contact.personDeleted` | object |  |
| `contact.personId` | object |  |
| `contact.photoUrl` | object |  |
| `contact.postalCode` | object |  |
| `contact.presentRawAddress` | object |  |
| `contact.queuedForCrmPush` | boolean |  |
| `contact.salesforceAccountId` | object |  |
| `contact.salesforceContactId` | object |  |
| `contact.salesforceId` | object |  |
| `contact.salesforceLeadId` | object |  |
| `contact.sanitizedPhone` | object |  |
| `contact.showIntent` | boolean |  |
| `contact.source` | string |  |
| `contact.sourceDisplayName` | string |  |
| `contact.state` | object |  |
| `contact.streetAddress` | object |  |
| `contact.suggestedFromRuleEngineConfigId` | object |  |
| `contact.timeZone` | object |  |
| `contact.title` | string |  |
| `contact.twitterUrl` | object |  |
| `contact.updatedAt` | date |  |
| `contact.updatedEmailTrueStatus` | boolean |  |

## Native endpoint

Through the native Apollo API, this operation is `POST v1/contacts` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-contact.md) for the provider-specific parameters and requirements.

