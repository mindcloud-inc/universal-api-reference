# Keap: Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/keap/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/keap/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keap/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addresses` | string | no |  |
| `anniversary_date` | string | no |  |
| `birth_date` | string | no |  |
| `company` | string | no |  |
| `contact_id` | string | yes | The unique identifier of the contact. |
| `contact_type` | string | no |  |
| `custom_fields` | string | no |  |
| `email_addresses` | string | no |  |
| `family_name` | string | no |  |
| `fax_numbers` | string | no |  |
| `fields` | string | no |  |
| `given_name` | string | no |  |
| `job_title` | string | no |  |
| `leadsource_id` | string | no |  |
| `middle_name` | string | no |  |
| `origin` | string | no |  |
| `owner_id` | string | no |  |
| `phone_numbers` | string | no |  |
| `preferred_locale` | string | no |  |
| `preferred_name` | string | no |  |
| `prefix` | string | no |  |
| `referral_code` | string | no |  |
| `social_accounts` | string | no |  |
| `source_type` | string | no |  |
| `spouse_name` | string | no |  |
| `suffix` | string | no |  |
| `time_zone` | string | no |  |
| `update_mask` | string | no |  |
| `utm_parameters` | string | no |  |
| `website` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {
          "country": "string",
          "countryCode": "string",
          "field": "string",
          "line1": "string",
          "line2": "string",
          "locality": "string",
          "postalCode": "string",
          "region": "string",
          "regionCode": "string",
          "zipCode": "string",
          "zipFour": "string"
        }
      ],
      "anniversaryDate": "string",
      "birthDate": "string",
      "company": {
        "companyName": "Ava Chen",
        "id": "string"
      },
      "contactType": "string",
      "createTime": "string",
      "customFields": [
        {
          "content": "string",
          "id": "string"
        }
      ],
      "emailAddresses": [
        {
          "email": "ava@example.com",
          "emailOptStatus": "ava@example.com",
          "field": "ava@example.com",
          "isOptIn": "ava@example.com",
          "optInReason": "ava@example.com"
        }
      ],
      "familyName": "Ava Chen",
      "faxNumbers": [
        {
          "field": "string",
          "number": "string",
          "type": "string"
        }
      ],
      "givenName": "Ava Chen",
      "id": "string",
      "jobTitle": "string",
      "leadsourceId": "string",
      "links": [
        {
          "id": "https://example.com",
          "linkedContactId": "https://example.com",
          "linkTypeId": "https://example.com",
          "linkTypeName": "https://example.com"
        }
      ],
      "middleName": "Ava Chen",
      "origin": {
        "date": "string",
        "ipAddress": "string"
      },
      "ownerId": "string",
      "phoneNumbers": [
        {
          "extension": "string",
          "field": "string",
          "number": "string",
          "numberE164": "string",
          "type": "string"
        }
      ],
      "preferredLocale": "string",
      "preferredName": "Ava Chen",
      "prefix": "string",
      "referralCode": "string",
      "scoreValue": "string",
      "socialAccounts": [
        {
          "name": "Ava Chen",
          "type": "string"
        }
      ],
      "sourceType": "string",
      "spouseName": "Ava Chen",
      "suffix": "string",
      "tagIds": [
        "string"
      ],
      "timeZone": "string",
      "updateTime": "string",
      "utmParameters": [
        {
          "dateCreated": "2026-05-07T12:00:00.000Z",
          "firstTouch": "string",
          "id": "string",
          "keapSourceId": "string",
          "lastTouch": "string",
          "utmCampaign": "string",
          "utmContent": "string",
          "utmMedium": "string",
          "utmSource": "string",
          "utmTerm": "string"
        }
      ],
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses[].country` | string |  |
| `addresses[].countryCode` | string |  |
| `addresses[].field` | string |  |
| `addresses[].line1` | string |  |
| `addresses[].line2` | string |  |
| `addresses[].locality` | string |  |
| `addresses[].postalCode` | string |  |
| `addresses[].region` | string |  |
| `addresses[].regionCode` | string |  |
| `addresses[].zipCode` | string |  |
| `addresses[].zipFour` | string |  |
| `anniversaryDate` | string |  |
| `birthDate` | string |  |
| `company.companyName` | string |  |
| `company.id` | string |  |
| `contactType` | string |  |
| `createTime` | string |  |
| `customFields[].content` | string |  |
| `customFields[].id` | string |  |
| `emailAddresses[].email` | string |  |
| `emailAddresses[].emailOptStatus` | string |  |
| `emailAddresses[].field` | string |  |
| `emailAddresses[].isOptIn` | string |  |
| `emailAddresses[].optInReason` | string |  |
| `familyName` | string |  |
| `faxNumbers[].field` | string |  |
| `faxNumbers[].number` | string |  |
| `faxNumbers[].type` | string |  |
| `givenName` | string |  |
| `id` | string |  |
| `jobTitle` | string |  |
| `leadsourceId` | string |  |
| `links[].id` | string |  |
| `links[].linkedContactId` | string |  |
| `links[].linkTypeId` | string |  |
| `links[].linkTypeName` | string |  |
| `middleName` | string |  |
| `origin.date` | string |  |
| `origin.ipAddress` | string |  |
| `ownerId` | string |  |
| `phoneNumbers[].extension` | string |  |
| `phoneNumbers[].field` | string |  |
| `phoneNumbers[].number` | string |  |
| `phoneNumbers[].numberE164` | string |  |
| `phoneNumbers[].type` | string |  |
| `preferredLocale` | string |  |
| `preferredName` | string |  |
| `prefix` | string |  |
| `referralCode` | string |  |
| `scoreValue` | string |  |
| `socialAccounts[].name` | string |  |
| `socialAccounts[].type` | string |  |
| `sourceType` | string |  |
| `spouseName` | string |  |
| `suffix` | string |  |
| `tagIds[]` | string |  |
| `timeZone` | string |  |
| `updateTime` | string |  |
| `utmParameters[].dateCreated` | date |  |
| `utmParameters[].firstTouch` | string |  |
| `utmParameters[].id` | string |  |
| `utmParameters[].keapSourceId` | string |  |
| `utmParameters[].lastTouch` | string |  |
| `utmParameters[].utmCampaign` | string |  |
| `utmParameters[].utmContent` | string |  |
| `utmParameters[].utmMedium` | string |  |
| `utmParameters[].utmSource` | string |  |
| `utmParameters[].utmTerm` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Keap API, this operation is `PATCH /contacts/{contact_id}` (base URL `https://api.infusionsoft.com/crm/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

