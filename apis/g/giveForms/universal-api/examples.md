# GiveForms Universal API Examples

These examples use the MindCloud API key and GiveForms connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Donations

Finds donations for your organization in GiveForms.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giveForms/latest/actions/list-donations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giveForms/latest/actions/list-donations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "amount": "string",
      "anonymous": true,
      "appFee": 1,
      "city": "string",
      "convertedAmount": "string",
      "convertedCurrency": "string",
      "country": "string",
      "currency": "string",
      "donationDate": "2026-05-07T12:00:00.000Z",
      "donationHonor": {},
      "donationType": "string",
      "email": "ava@example.com",
      "expMonth": 1,
      "expYear": 1,
      "feeCovered": "string",
      "firstName": "Ava",
      "formattedAmount": "string",
      "formattedAppFee": "string",
      "formattedConvertedAmount": "string",
      "formattedProcessingFee": "string",
      "formName": "Ava Chen",
      "id": 1,
      "last4": "string",
      "lastName": "Chen",
      "lastUpdatedAt": "2026-05-07T12:00:00.000Z",
      "paymentChargeId": "string",
      "paymentType": "string",
      "postcode": "string",
      "processingFee": 1,
      "questions": [
        {}
      ],
      "recurring": true,
      "state": "string",
      "status": "string",
      "timezone": "string",
      "utmCampaign": "string",
      "utmContent": "string",
      "utmMedium": "string",
      "utmSource": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Donations action reference](actions/list-donations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/giveForms/latest/actions/list-donations).
