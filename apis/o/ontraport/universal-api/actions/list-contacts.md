# Ontraport: List Contacts

Retrieves a list of contacts from Ontraport.

```
GET https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ontraport `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/list-contacts?${params}`, {
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
| `search` | string | no | Search the contact collection for a string. |
| `searchNotes` | boolean | no | Search notes for the search string. |
| `condition` | string | no | JSON-encoded filter criteria for selecting contacts. |
| `listFields` | string | no | Comma-delimited list of contact fields to return. |
| `externs` | string | no | Comma-delimited list of related external fields to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "address2": "string",
      "affAmount": "string",
      "affPaypal": "string",
      "affSales": "string",
      "bindex": "string",
      "birthday": "2026-05-07T12:00:00.000Z",
      "bulkMail": "string",
      "bulkSms": "string",
      "ccExpirationDate": "2026-05-07T12:00:00.000Z",
      "ccExpirationMonth": "string",
      "ccExpirationYear": "string",
      "ccNumber": "string",
      "ccType": "string",
      "city": "string",
      "commish": "string",
      "company": "string",
      "contactCat": "string",
      "country": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "dla": "2026-05-07T12:00:00.000Z",
      "dlm": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "f2110": "2026-05-07T12:00:00.000Z",
      "facebookLink": "https://example.com",
      "fax": "string",
      "fbc": "string",
      "fbGender": "string",
      "fbp": "string",
      "firstname": "Ava",
      "freferrer": "string",
      "gcid": "string",
      "gclid": "string",
      "grade": "string",
      "gsid": "string",
      "gsn": "string",
      "hasMembership": "string",
      "homePhone": "string",
      "id": "string",
      "importId": "string",
      "instagramLink": "https://example.com",
      "ipAddy": "string",
      "ipAddyDisplay": "string",
      "lastCurrencyUsed": "string",
      "lastInboundSms": "string",
      "lastname": "Chen",
      "lCampaign": "string",
      "lContent": "string",
      "lead": "string",
      "liFatId": "string",
      "linkedinLink": "https://example.com",
      "lLeadSource": "string",
      "lMedium": "string",
      "lreferrer": "string",
      "lTerm": "string",
      "mrcAmount": "string",
      "mrcResult": "string",
      "mrcUnpaid": "string",
      "mriInvoiceNum": "string",
      "mriInvoiceTotal": "string",
      "nCampaign": "string",
      "nContent": "string",
      "nLeadSource": "string",
      "nMedia": "string",
      "nMedium": "string",
      "nTerm": "string",
      "numPurchased": "string",
      "officePhone": "string",
      "owed": "string",
      "owner": "string",
      "priority": "string",
      "profileImage": "string",
      "programId": "string",
      "referralPage": "string",
      "refund": "string",
      "refundtotal": "string",
      "smsNumber": "string",
      "sourceLocation": "string",
      "spent": "string",
      "state": "string",
      "status": "string",
      "systemSource": "string",
      "timeSinceDla": "string",
      "timezone": "string",
      "title": "string",
      "twitterLink": "https://example.com",
      "uniqueId": "string",
      "unpaidInvoices": "string",
      "userAgent": "string",
      "visit": "string",
      "website": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `address2` | string |  |
| `affAmount` | string |  |
| `affPaypal` | string |  |
| `affSales` | string |  |
| `bindex` | string |  |
| `birthday` | date |  |
| `bulkMail` | string |  |
| `bulkSms` | string |  |
| `ccExpirationDate` | date |  |
| `ccExpirationMonth` | string |  |
| `ccExpirationYear` | string |  |
| `ccNumber` | string |  |
| `ccType` | string |  |
| `city` | string |  |
| `commish` | string |  |
| `company` | string |  |
| `contactCat` | string |  |
| `country` | string |  |
| `date` | date |  |
| `dla` | date |  |
| `dlm` | date |  |
| `email` | string |  |
| `f2110` | date |  |
| `facebookLink` | string |  |
| `fax` | string |  |
| `fbc` | string |  |
| `fbGender` | string |  |
| `fbp` | string |  |
| `firstname` | string |  |
| `freferrer` | string |  |
| `gcid` | string |  |
| `gclid` | string |  |
| `grade` | string |  |
| `gsid` | string |  |
| `gsn` | string |  |
| `hasMembership` | string |  |
| `homePhone` | string |  |
| `id` | string |  |
| `importId` | string |  |
| `instagramLink` | string |  |
| `ipAddy` | string |  |
| `ipAddyDisplay` | string |  |
| `lastCurrencyUsed` | string |  |
| `lastInboundSms` | string |  |
| `lastname` | string |  |
| `lCampaign` | string |  |
| `lContent` | string |  |
| `lead` | string |  |
| `liFatId` | string |  |
| `linkedinLink` | string |  |
| `lLeadSource` | string |  |
| `lMedium` | string |  |
| `lreferrer` | string |  |
| `lTerm` | string |  |
| `mrcAmount` | string |  |
| `mrcResult` | string |  |
| `mrcUnpaid` | string |  |
| `mriInvoiceNum` | string |  |
| `mriInvoiceTotal` | string |  |
| `nCampaign` | string |  |
| `nContent` | string |  |
| `nLeadSource` | string |  |
| `nMedia` | string |  |
| `nMedium` | string |  |
| `nTerm` | string |  |
| `numPurchased` | string |  |
| `officePhone` | string |  |
| `owed` | string |  |
| `owner` | string |  |
| `priority` | string |  |
| `profileImage` | string |  |
| `programId` | string |  |
| `referralPage` | string |  |
| `refund` | string |  |
| `refundtotal` | string |  |
| `smsNumber` | string |  |
| `sourceLocation` | string |  |
| `spent` | string |  |
| `state` | string |  |
| `status` | string |  |
| `systemSource` | string |  |
| `timeSinceDla` | string |  |
| `timezone` | string |  |
| `title` | string |  |
| `twitterLink` | string |  |
| `uniqueId` | string |  |
| `unpaidInvoices` | string |  |
| `userAgent` | string |  |
| `visit` | string |  |
| `website` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native Ontraport API, this operation is `GET /Contacts` (base URL `https://api.ontraport.com/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

