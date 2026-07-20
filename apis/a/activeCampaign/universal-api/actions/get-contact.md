# ActiveCampaign: Get Contact

Retrieves a contact from ActiveCampaign.

```
GET https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveCampaign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/get-contact?${params}`, {
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
| `id` | number | yes | The contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "adate": "2026-05-07T12:00:00.000Z",
        "anonymized": "string",
        "bestSendHour": {},
        "bouncedDate": "2026-05-07T12:00:00.000Z",
        "bouncedHard": "string",
        "bouncedSoft": "string",
        "cdate": "2026-05-07T12:00:00.000Z",
        "contactLists": [
          "string"
        ],
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
          "accountContacts": "https://example.com",
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
        "socialdataLastcheck": {},
        "ua": {},
        "udate": "2026-05-07T12:00:00.000Z",
        "updatedBy": {},
        "updatedTimestamp": "2026-05-07T12:00:00.000Z",
        "updatedUtcTimestamp": "2026-05-07T12:00:00.000Z"
      },
      "contactLists": [
        {
          "automation": {},
          "autosyncLog": {},
          "campaign": {},
          "channel": "string",
          "contact": "string",
          "createdBy": {},
          "createdTimestamp": "2026-05-07T12:00:00.000Z",
          "firstName": "Ava",
          "form": {},
          "id": "string",
          "ip4Last": "string",
          "ip4Sub": "string",
          "ip4Unsub": "string",
          "lastName": "Chen",
          "links": {
            "automation": "https://example.com",
            "autosyncLog": "https://example.com",
            "campaign": "https://example.com",
            "contact": "https://example.com",
            "form": "https://example.com",
            "list": "https://example.com",
            "message": "https://example.com",
            "unsubscribeAutomation": "https://example.com"
          },
          "list": "string",
          "message": {},
          "responder": "string",
          "sdate": "2026-05-07T12:00:00.000Z",
          "seriesid": "string",
          "sourceid": "string",
          "status": "string",
          "sync": "string",
          "udate": "2026-05-07T12:00:00.000Z",
          "unsubreason": "string",
          "unsubscribeAutomation": {},
          "updatedBy": {},
          "updatedTimestamp": "2026-05-07T12:00:00.000Z"
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
| `contact.adate` | date |  |
| `contact.anonymized` | string |  |
| `contact.bestSendHour` | object |  |
| `contact.bouncedDate` | date |  |
| `contact.bouncedHard` | string |  |
| `contact.bouncedSoft` | string |  |
| `contact.cdate` | date |  |
| `contact.contactLists[]` | string |  |
| `contact.createdBy` | object |  |
| `contact.createdTimestamp` | date |  |
| `contact.createdUtcTimestamp` | date |  |
| `contact.deleted` | string |  |
| `contact.deletedAt` | date |  |
| `contact.edate` | date |  |
| `contact.email` | string |  |
| `contact.emailDomain` | string |  |
| `contact.emailLocal` | string |  |
| `contact.firstName` | string |  |
| `contact.gravatar` | string |  |
| `contact.hash` | string |  |
| `contact.id` | string |  |
| `contact.ip` | string |  |
| `contact.lastClickDate` | date |  |
| `contact.lastMppOpenDate` | date |  |
| `contact.lastName` | string |  |
| `contact.lastOpenDate` | date |  |
| `contact.links.accountContacts` | string |  |
| `contact.links.automationEntryCounts` | string |  |
| `contact.links.bounceLogs` | string |  |
| `contact.links.contactAutomations` | string |  |
| `contact.links.contactData` | string |  |
| `contact.links.contactDeals` | string |  |
| `contact.links.contactGoals` | string |  |
| `contact.links.contactLists` | string |  |
| `contact.links.contactLogs` | string |  |
| `contact.links.contactTags` | string |  |
| `contact.links.deals` | string |  |
| `contact.links.fieldValues` | string |  |
| `contact.links.geoIps` | string |  |
| `contact.links.notes` | string |  |
| `contact.links.organization` | string |  |
| `contact.links.plusAppend` | string |  |
| `contact.links.scoreValues` | string |  |
| `contact.links.trackingLogs` | string |  |
| `contact.mppTracking` | string |  |
| `contact.organization` | object |  |
| `contact.orgid` | string |  |
| `contact.orgname` | string |  |
| `contact.phone` | string |  |
| `contact.ratingTstamp` | object |  |
| `contact.segmentioId` | string |  |
| `contact.sentcnt` | string |  |
| `contact.socialdataLastcheck` | object |  |
| `contact.ua` | object |  |
| `contact.udate` | date |  |
| `contact.updatedBy` | object |  |
| `contact.updatedTimestamp` | date |  |
| `contact.updatedUtcTimestamp` | date |  |
| `contactLists[].automation` | object |  |
| `contactLists[].autosyncLog` | object |  |
| `contactLists[].campaign` | object |  |
| `contactLists[].channel` | string |  |
| `contactLists[].contact` | string |  |
| `contactLists[].createdBy` | object |  |
| `contactLists[].createdTimestamp` | date |  |
| `contactLists[].firstName` | string |  |
| `contactLists[].form` | object |  |
| `contactLists[].id` | string |  |
| `contactLists[].ip4Last` | string |  |
| `contactLists[].ip4Sub` | string |  |
| `contactLists[].ip4Unsub` | string |  |
| `contactLists[].lastName` | string |  |
| `contactLists[].links.automation` | string |  |
| `contactLists[].links.autosyncLog` | string |  |
| `contactLists[].links.campaign` | string |  |
| `contactLists[].links.contact` | string |  |
| `contactLists[].links.form` | string |  |
| `contactLists[].links.list` | string |  |
| `contactLists[].links.message` | string |  |
| `contactLists[].links.unsubscribeAutomation` | string |  |
| `contactLists[].list` | string |  |
| `contactLists[].message` | object |  |
| `contactLists[].responder` | string |  |
| `contactLists[].sdate` | date |  |
| `contactLists[].seriesid` | string |  |
| `contactLists[].sourceid` | string |  |
| `contactLists[].status` | string |  |
| `contactLists[].sync` | string |  |
| `contactLists[].udate` | date |  |
| `contactLists[].unsubreason` | string |  |
| `contactLists[].unsubscribeAutomation` | object |  |
| `contactLists[].updatedBy` | object |  |
| `contactLists[].updatedTimestamp` | date |  |

## Native endpoint

Through the native ActiveCampaign API, this operation is `GET /contacts/:id` (base URL `{{credentials.apiUrl}}/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

