# ActiveCampaign Universal API Examples

These examples use the MindCloud API key and ActiveCampaign connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves contacts from ActiveCampaign.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/list-contacts?${params}`, {
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
      "adate": "2026-05-07T12:00:00.000Z",
      "anonymized": "string",
      "bestSendHour": {},
      "bouncedDate": "2026-05-07T12:00:00.000Z",
      "bouncedHard": "string",
      "bouncedSoft": "string",
      "cdate": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "createdTimestamp": "2026-05-07T12:00:00.000Z",
      "createdUtcTimestamp": "2026-05-07T12:00:00.000Z",
      "deleted": "string",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "edate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emailDomain": "ava@example.com",
      "emailLocal": "ava@example.com",
      "firstName": "Ava",
      "gravatar": "string",
      "hash": "string",
      "id": "string",
      "ip": "string",
      "lastClickDate": "2026-05-07T12:00:00.000Z",
      "lastMppOpenDate": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "lastOpenDate": "2026-05-07T12:00:00.000Z",
      "links": {
        "automationEntryCounts": "https://example.com",
        "bounceLogs": "https://example.com",
        "contactAutomations": "https://example.com",
        "contactData": "https://example.com",
        "contactDeals": "https://example.com",
        "contactGoals": "https://example.com",
        "contactLists": "https://example.com",
        "contactLogs": "https://example.com",
        "contactTags": "https://example.com",
        "deals": "https://example.com",
        "fieldValues": "https://example.com",
        "geoIps": "https://example.com",
        "notes": "https://example.com",
        "organization": "https://example.com",
        "plusAppend": "https://example.com",
        "scoreValues": "https://example.com",
        "trackingLogs": "https://example.com"
      },
      "mppTracking": "string",
      "organization": {},
      "orgid": "string",
      "orgname": "Ava Chen",
      "phone": "string",
      "ratingTstamp": {},
      "segmentioId": "string",
      "sentcnt": "string",
      "smsConsent": {},
      "smsConsentUpdatedAt": "2026-05-07T12:00:00.000Z",
      "socialdataLastcheck": {},
      "ua": {},
      "udate": "2026-05-07T12:00:00.000Z",
      "updatedBy": {},
      "updatedTimestamp": "2026-05-07T12:00:00.000Z",
      "updatedUtcTimestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/activeCampaign/latest/actions/list-contacts).

## Add Contact To Automation

Adds a contact to an automation in ActiveCampaign.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/add-contact-to-automation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactAutomation.contact": 1,
  "contactAutomation.automation": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/add-contact-to-automation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactAutomation.contact": 1,
    "contactAutomation.automation": 1
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Contact To Automation action reference](actions/add-contact-to-automation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/activeCampaign/latest/actions/add-contact-to-automation).
