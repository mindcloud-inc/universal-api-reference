# Cliengo Universal API Examples

These examples use the MindCloud API key and Cliengo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/get-account?${params}`, {
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
      "chatUrl": "https://example.com",
      "contactName": "Ava Chen",
      "countryId": "string",
      "creationDate": "string",
      "email": "ava@example.com",
      "freeTrialExpirationDate": "string",
      "hasConversationPlan": true,
      "hasSubscription": true,
      "id": "string",
      "labs": {},
      "language": "string",
      "leadCount": 1,
      "leadCountTotal": 1,
      "leadLimit": 1,
      "marketingCampaignsInfo": {},
      "name": "Ava Chen",
      "phone": "string",
      "planCurrency": "string",
      "planFrequency": "string",
      "planLimits": [
        {}
      ],
      "planName": "Ava Chen",
      "planPrice": 1,
      "planShortName": "Ava Chen",
      "planType": "string",
      "quickstartSteps": {},
      "tags": {},
      "timeZone": "string",
      "userCount": 1,
      "whiteLabelEmail": "ava@example.com",
      "whiteLabelId": "string",
      "whiteLabelLogoUrl": "https://example.com",
      "whiteLabelName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cliengo/latest/actions/get-account).

## Add Contact Tags



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/add-contact-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "tag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/add-contact-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "tag": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "accountName": "Ava Chen",
      "age": 1,
      "calls": [
        "string"
      ],
      "creationDate": "2026-05-07T12:00:00.000Z",
      "duplicatedContact": true,
      "email": "ava@example.com",
      "entryMethod": "string",
      "geoip": {},
      "id": "string",
      "lastName": "Chen",
      "lastUpdateDate": "2026-05-07T12:00:00.000Z",
      "leadFields": {},
      "logs": [
        "string"
      ],
      "medium": "string",
      "mediumTranslate": "string",
      "message": "string",
      "name": "Ava Chen",
      "notes": [
        "string"
      ],
      "phone": "string",
      "rating": 1,
      "status": "string",
      "subStatus": "string",
      "utmCampaign": "string",
      "utmContent": "string",
      "utmMedium": "string",
      "utmTerm": "string",
      "websiteId": "string",
      "websiteName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Add Contact Tags action reference](actions/add-contact-tags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cliengo/latest/actions/add-contact-tags).
