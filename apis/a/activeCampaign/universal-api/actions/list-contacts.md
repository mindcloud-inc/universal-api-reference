# ActiveCampaign: List Contacts

Retrieves contacts from ActiveCampaign.

```
GET https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveCampaign `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `search` | string | no | Search contacts by name, organization, phone, or email. |
| `email` | string | no | Filter contacts by exact email. |
| `listId` | string | no | Filter contacts associated with a specific list. |
| `segmentId` | string | no | Return contacts that match the specified list segment. |
| `status` | number | no | Filter by contact status value. |
| `formId` | number | no | Filter contacts associated with a form. |
| `idGreater` | number | no | Only include contacts with ID greater than this value. |
| `idLess` | number | no | Only include contacts with ID less than this value. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adate` | date |  |
| `anonymized` | string |  |
| `bestSendHour` | object |  |
| `bouncedDate` | date |  |
| `bouncedHard` | string |  |
| `bouncedSoft` | string |  |
| `cdate` | date |  |
| `createdBy` | object |  |
| `createdTimestamp` | date |  |
| `createdUtcTimestamp` | date |  |
| `deleted` | string |  |
| `deletedAt` | date |  |
| `edate` | date |  |
| `email` | string |  |
| `emailDomain` | string |  |
| `emailLocal` | string |  |
| `firstName` | string |  |
| `gravatar` | string |  |
| `hash` | string |  |
| `id` | string |  |
| `ip` | string |  |
| `lastClickDate` | date |  |
| `lastMppOpenDate` | date |  |
| `lastName` | string |  |
| `lastOpenDate` | date |  |
| `links.automationEntryCounts` | string |  |
| `links.bounceLogs` | string |  |
| `links.contactAutomations` | string |  |
| `links.contactData` | string |  |
| `links.contactDeals` | string |  |
| `links.contactGoals` | string |  |
| `links.contactLists` | string |  |
| `links.contactLogs` | string |  |
| `links.contactTags` | string |  |
| `links.deals` | string |  |
| `links.fieldValues` | string |  |
| `links.geoIps` | string |  |
| `links.notes` | string |  |
| `links.organization` | string |  |
| `links.plusAppend` | string |  |
| `links.scoreValues` | string |  |
| `links.trackingLogs` | string |  |
| `mppTracking` | string |  |
| `organization` | object |  |
| `orgid` | string |  |
| `orgname` | string |  |
| `phone` | string |  |
| `ratingTstamp` | object |  |
| `segmentioId` | string |  |
| `sentcnt` | string |  |
| `smsConsent` | object |  |
| `smsConsentUpdatedAt` | date |  |
| `socialdataLastcheck` | object |  |
| `ua` | object |  |
| `udate` | date |  |
| `updatedBy` | object |  |
| `updatedTimestamp` | date |  |
| `updatedUtcTimestamp` | date |  |

## Native endpoint

Through the native ActiveCampaign API, this operation is `GET /contacts` (base URL `{{credentials.apiUrl}}/api/3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

