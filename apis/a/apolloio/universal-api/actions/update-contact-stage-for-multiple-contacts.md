# Apollo: Update Contact Stage for Multiple Contacts

Updates contact stages for multiple contacts in Apollo.

```
PUT https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/update-contact-stage-for-multiple-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/update-contact-stage-for-multiple-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactIds[]": [
    "string"
  ],
  "contactStageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/update-contact-stage-for-multiple-contacts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactIds[]": ["string"],
    "contactStageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactIds[]` | array<string> | yes | The Apollo IDs for the contacts that you want to update. To find contact IDs, call the Search for Contacts endpoint and identify the `id` value for the contact. Example: `66e34b81740c50074e3d1bd4` Accepts multiple values as an array. |
| `contactStageId` | string<string> | yes | The Apollo ID for the contact stage to which you want to assign the contacts. Call the List Contact Stages endpoint to retrieve a list of all the contact stage IDs available in your Apollo account. Example: `6095a710bd01d100a506d4af` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "accountPhoneNote": {},
      "callOptedOut": {},
      "contactStageId": "string",
      "createdAt": "string",
      "creatorId": "string",
      "crmId": {},
      "crmOwnerId": {},
      "crmRecordUrl": {},
      "customFieldErrors": {},
      "directDialEnrichmentFailedAt": {},
      "directDialStatus": {},
      "email": "ava@example.com",
      "emailDomainCatchall": true,
      "emailFromCustomer": {},
      "emailNeedsTickling": true,
      "emailSource": "ava@example.com",
      "emailStatus": "ava@example.com",
      "emailStatusUnavailableReason": {},
      "emailTrueStatus": "ava@example.com",
      "emailUnsubscribed": {},
      "existenceLevel": "string",
      "extrapolatedEmailConfidence": {},
      "firstName": "Ava",
      "freeDomain": true,
      "hasEmailArcgateRequest": true,
      "hasPendingEmailArcgateRequest": true,
      "headline": "string",
      "hubspotCompanyId": {},
      "hubspotVid": {},
      "id": "string",
      "intentStrength": {},
      "labelIds": [
        "string"
      ],
      "lastActivityDate": {},
      "lastName": "Chen",
      "linkedinUid": {},
      "linkedinUrl": "https://example.com",
      "mergedCrmIds": {},
      "name": "Ava Chen",
      "organizationId": "string",
      "organizationName": "Ava Chen",
      "originalSource": "string",
      "ownerId": "string",
      "personDeleted": {},
      "personId": "string",
      "phoneNumbers": [
        {
          "dialerFlags": {
            "countryEnabled": true,
            "countryName": "Ava Chen",
            "highRiskCallingEnabled": true,
            "potentialHighRiskNumber": true
          },
          "dncOtherInfo": {},
          "dncStatus": {},
          "position": 1,
          "rawNumber": "string",
          "sanitizedNumber": "string",
          "sourceName": "Ava Chen",
          "status": "string",
          "thirdPartyVendorName": {},
          "type": "string"
        }
      ],
      "photoUrl": {},
      "presentRawAddress": "string",
      "queuedForCrmPush": {},
      "salesforceAccountId": {},
      "salesforceContactId": {},
      "salesforceId": {},
      "salesforceLeadId": {},
      "sanitizedPhone": "string",
      "showIntent": true,
      "source": "string",
      "sourceDisplayName": "Ava Chen",
      "suggestedFromRuleEngineConfigId": {},
      "timeZone": "string",
      "title": "string",
      "twitterUrl": {},
      "updatedAt": "string",
      "updatedEmailTrueStatus": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `accountPhoneNote` | object |  |
| `callOptedOut` | object |  |
| `contactStageId` | string |  |
| `createdAt` | string |  |
| `creatorId` | string |  |
| `crmId` | object |  |
| `crmOwnerId` | object |  |
| `crmRecordUrl` | object |  |
| `customFieldErrors` | object |  |
| `directDialEnrichmentFailedAt` | object |  |
| `directDialStatus` | object |  |
| `email` | string |  |
| `emailDomainCatchall` | boolean |  |
| `emailFromCustomer` | object |  |
| `emailNeedsTickling` | boolean |  |
| `emailSource` | string |  |
| `emailStatus` | string |  |
| `emailStatusUnavailableReason` | object |  |
| `emailTrueStatus` | string |  |
| `emailUnsubscribed` | object |  |
| `existenceLevel` | string |  |
| `extrapolatedEmailConfidence` | object |  |
| `firstName` | string |  |
| `freeDomain` | boolean |  |
| `hasEmailArcgateRequest` | boolean |  |
| `hasPendingEmailArcgateRequest` | boolean |  |
| `headline` | string |  |
| `hubspotCompanyId` | object |  |
| `hubspotVid` | object |  |
| `id` | string |  |
| `intentStrength` | object |  |
| `labelIds[]` | string |  |
| `lastActivityDate` | object |  |
| `lastName` | string |  |
| `linkedinUid` | object |  |
| `linkedinUrl` | string |  |
| `mergedCrmIds` | object |  |
| `name` | string |  |
| `organizationId` | string |  |
| `organizationName` | string |  |
| `originalSource` | string |  |
| `ownerId` | string |  |
| `personDeleted` | object |  |
| `personId` | string |  |
| `phoneNumbers[].dialerFlags.countryEnabled` | boolean |  |
| `phoneNumbers[].dialerFlags.countryName` | string |  |
| `phoneNumbers[].dialerFlags.highRiskCallingEnabled` | boolean |  |
| `phoneNumbers[].dialerFlags.potentialHighRiskNumber` | boolean |  |
| `phoneNumbers[].dncOtherInfo` | object |  |
| `phoneNumbers[].dncStatus` | object |  |
| `phoneNumbers[].position` | number |  |
| `phoneNumbers[].rawNumber` | string |  |
| `phoneNumbers[].sanitizedNumber` | string |  |
| `phoneNumbers[].sourceName` | string |  |
| `phoneNumbers[].status` | string |  |
| `phoneNumbers[].thirdPartyVendorName` | object |  |
| `phoneNumbers[].type` | string |  |
| `photoUrl` | object |  |
| `presentRawAddress` | string |  |
| `queuedForCrmPush` | object |  |
| `salesforceAccountId` | object |  |
| `salesforceContactId` | object |  |
| `salesforceId` | object |  |
| `salesforceLeadId` | object |  |
| `sanitizedPhone` | string |  |
| `showIntent` | boolean |  |
| `source` | string |  |
| `sourceDisplayName` | string |  |
| `suggestedFromRuleEngineConfigId` | object |  |
| `timeZone` | string |  |
| `title` | string |  |
| `twitterUrl` | object |  |
| `updatedAt` | string |  |
| `updatedEmailTrueStatus` | boolean |  |

## Native endpoint

Through the native Apollo API, this operation is `POST v1/contacts/update_stages` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-stage-for-multiple-contacts.md) for the provider-specific parameters and requirements.

