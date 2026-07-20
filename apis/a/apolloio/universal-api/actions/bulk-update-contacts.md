# Apollo: Bulk Update Contacts

Updates multiple existing contacts in Apollo.

```
PUT https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/bulk-update-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/bulk-update-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactAttributes[].id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/bulk-update-contacts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactAttributes[].id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactIds[]` | array<string> | no | Array of contact IDs to update with the same values. Use this for applying the same updates to multiple contacts. |
| `contactAttributes[]` | array<object> | no | Array of contact objects with individual updates. Use this for applying different updates to each contact. |
| `contactAttributes[].id` | string | yes | The contact ID to update |
| `contactAttributes[].firstName` | string | no | The contact's first name |
| `contactAttributes[].lastName` | string | no | The contact's last name |
| `contactAttributes[].email` | string | no | The contact's email address |
| `contactAttributes[].title` | string | no | The contact's job title |
| `contactAttributes[].organizationName` | string | no | The contact's organization name |
| `contactAttributes[].ownerId` | string | no | The Apollo user ID to assign as owner |
| `contactAttributes[].accountId` | string | no | The Apollo account ID to associate with the contact |
| `contactAttributes[].presentRawAddress` | string | no | The contact's location |
| `contactAttributes[].linkedinUrl` | string | no | The contact's LinkedIn profile URL |
| `contactAttributes[].typedCustomFields` | object | no | Custom field values as key-value pairs |
| `ownerId` | string | no | When using contact_ids, apply this owner to all contacts |
| `email` | string | no | When using contact_ids, apply this email to all contacts |
| `organizationName` | string | no | When using contact_ids, apply this organization name to all contacts |
| `title` | string | no | When using contact_ids, apply this title to all contacts |
| `firstName` | string | no | When using contact_ids, apply this first name to all contacts |
| `lastName` | string | no | When using contact_ids, apply this last name to all contacts |
| `accountId` | string | no | When using contact_ids, apply this account ID to all contacts |
| `presentRawAddress` | string | no | When using contact_ids, apply this address to all contacts |
| `linkedinUrl` | string | no | When using contact_ids, apply this LinkedIn URL to all contacts |
| `typedCustomFields` | object | no | When using contact_ids, apply these custom fields to all contacts |
| `async` | boolean | no | Force asynchronous processing. Automatically enabled for >100 contacts. |
| `visibleEntityIds[]` | array<string> | no | Specific contact IDs to return in the response (for performance) |

## Response

```json
{
  "success": true,
  "data": [
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | object |  |
| `accountPhoneNote` | object |  |
| `callOptedOut` | object |  |
| `city` | object |  |
| `contactEmails[].email` | string |  |
| `contactEmails[].emailMd5` | string |  |
| `contactEmails[].emailNeedsTickling` | boolean |  |
| `contactEmails[].emailSha256` | string |  |
| `contactEmails[].emailStatus` | string |  |
| `contactEmails[].emailStatusUnavailableReason` | object |  |
| `contactEmails[].emailTrueStatus` | string |  |
| `contactEmails[].extrapolatedEmailConfidence` | object |  |
| `contactEmails[].freeDomain` | boolean |  |
| `contactEmails[].position` | number |  |
| `contactEmails[].source` | string |  |
| `contactEmails[].thirdPartyVendorName` | object |  |
| `contactStageId` | string |  |
| `country` | object |  |
| `createdAt` | date |  |
| `creatorId` | string |  |
| `crmId` | object |  |
| `crmOwnerId` | object |  |
| `crmRecordUrl` | object |  |
| `customFieldErrors` | object |  |
| `directDialEnrichmentFailedAt` | object |  |
| `directDialStatus` | object |  |
| `email` | string |  |
| `emailDomainCatchall` | boolean |  |
| `emailFromCustomer` | boolean |  |
| `emailNeedsTickling` | boolean |  |
| `emailSource` | object |  |
| `emailStatus` | string |  |
| `emailStatusUnavailableReason` | object |  |
| `emailTrueStatus` | string |  |
| `emailUnsubscribed` | object |  |
| `existenceLevel` | string |  |
| `extrapolatedEmailConfidence` | object |  |
| `facebookUrl` | object |  |
| `firstName` | string |  |
| `formattedAddress` | object |  |
| `freeDomain` | boolean |  |
| `hasEmailArcgateRequest` | boolean |  |
| `hasPendingEmailArcgateRequest` | boolean |  |
| `headline` | object |  |
| `hubspotCompanyId` | object |  |
| `hubspotVid` | object |  |
| `id` | string |  |
| `intentStrength` | object |  |
| `lastActivityDate` | object |  |
| `lastName` | string |  |
| `linkedinUid` | object |  |
| `linkedinUrl` | object |  |
| `mergedCrmIds` | object |  |
| `name` | string |  |
| `organizationId` | string |  |
| `organizationName` | string |  |
| `originalSource` | string |  |
| `ownerId` | string |  |
| `personDeleted` | object |  |
| `personId` | object |  |
| `photoUrl` | object |  |
| `postalCode` | object |  |
| `presentRawAddress` | object |  |
| `queuedForCrmPush` | object |  |
| `salesforceAccountId` | object |  |
| `salesforceContactId` | object |  |
| `salesforceId` | object |  |
| `salesforceLeadId` | object |  |
| `sanitizedPhone` | object |  |
| `showIntent` | boolean |  |
| `source` | string |  |
| `sourceDisplayName` | string |  |
| `state` | object |  |
| `streetAddress` | object |  |
| `suggestedFromRuleEngineConfigId` | object |  |
| `timeZone` | object |  |
| `title` | string |  |
| `twitterUrl` | object |  |
| `updatedAt` | date |  |
| `updatedEmailTrueStatus` | boolean |  |

## Native endpoint

Through the native Apollo API, this operation is `POST v1/contacts/bulk_update` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-contacts.md) for the provider-specific parameters and requirements.

