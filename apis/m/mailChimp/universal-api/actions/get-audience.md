# Mailchimp: Get Audience

Retrieves an audience from Mailchimp.

```
GET https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-audience
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-audience?connectionId=$CONNECTION_ID&list_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "list_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-audience?${params}`, {
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
| `exclude_fields` | string | no |  |
| `fields` | string | no |  |
| `include_total_contacts` | boolean | no |  |
| `list_id` | string | yes | The unique ID for the Mailchimp audience. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "beamerAddress": "string",
      "campaignDefaults": {
        "fromEmail": "ava@example.com",
        "fromName": "Ava Chen",
        "language": "string",
        "subject": "string"
      },
      "contact": {
        "address1": "string",
        "address2": "string",
        "city": "string",
        "company": "string",
        "country": "string",
        "phone": "string",
        "state": "string",
        "zip": "string"
      },
      "dateCreated": "string",
      "doubleOptin": true,
      "emailTypeOption": true,
      "hasWelcome": true,
      "id": "string",
      "links": [
        [
          {}
        ]
      ],
      "listRating": 1,
      "marketingPermissions": true,
      "modules": [
        [
          "string"
        ]
      ],
      "name": "Ava Chen",
      "notifyOnSubscribe": "string",
      "notifyOnUnsubscribe": "string",
      "permissionReminder": "string",
      "stats": {
        "avgSubRate": 1,
        "avgUnsubRate": 1,
        "campaignCount": 1,
        "campaignLastSent": "string",
        "cleanedCount": 1,
        "cleanedCountSinceSend": 1,
        "clickRate": 1,
        "lastSubDate": "string",
        "lastUnsubDate": "string",
        "memberCount": 1,
        "memberCountSinceSend": 1,
        "mergeFieldCount": 1,
        "openRate": 1,
        "targetSubRate": 1,
        "unsubscribeCount": 1,
        "unsubscribeCountSinceSend": 1
      },
      "subscribeUrlLong": "https://example.com",
      "subscribeUrlShort": "https://example.com",
      "useArchiveBar": true,
      "visibility": "string",
      "webId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `beamerAddress` | string |  |
| `campaignDefaults` | object |  |
| `campaignDefaults.fromEmail` | string |  |
| `campaignDefaults.fromName` | string |  |
| `campaignDefaults.language` | string |  |
| `campaignDefaults.subject` | string |  |
| `contact` | object |  |
| `contact.address1` | string |  |
| `contact.address2` | string |  |
| `contact.city` | string |  |
| `contact.company` | string |  |
| `contact.country` | string |  |
| `contact.phone` | string |  |
| `contact.state` | string |  |
| `contact.zip` | string |  |
| `dateCreated` | string |  |
| `doubleOptin` | boolean |  |
| `emailTypeOption` | boolean |  |
| `hasWelcome` | boolean |  |
| `id` | string |  |
| `links[]` | array<object> |  |
| `links[].href` | string |  |
| `links[].method` | string |  |
| `links[].rel` | string |  |
| `links[].targetSchema` | string |  |
| `listRating` | number |  |
| `marketingPermissions` | boolean |  |
| `modules[]` | array<string> |  |
| `name` | string |  |
| `notifyOnSubscribe` | string |  |
| `notifyOnUnsubscribe` | string |  |
| `permissionReminder` | string |  |
| `stats` | object |  |
| `stats.avgSubRate` | number |  |
| `stats.avgUnsubRate` | number |  |
| `stats.campaignCount` | number |  |
| `stats.campaignLastSent` | string |  |
| `stats.cleanedCount` | number |  |
| `stats.cleanedCountSinceSend` | number |  |
| `stats.clickRate` | number |  |
| `stats.lastSubDate` | string |  |
| `stats.lastUnsubDate` | string |  |
| `stats.memberCount` | number |  |
| `stats.memberCountSinceSend` | number |  |
| `stats.mergeFieldCount` | number |  |
| `stats.openRate` | number |  |
| `stats.targetSubRate` | number |  |
| `stats.unsubscribeCount` | number |  |
| `stats.unsubscribeCountSinceSend` | number |  |
| `subscribeUrlLong` | string |  |
| `subscribeUrlShort` | string |  |
| `useArchiveBar` | boolean |  |
| `visibility` | string |  |
| `webId` | number |  |

## Native endpoint

Through the native Mailchimp API, this operation is `GET lists/:list_id` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-audience.md) for the provider-specific parameters and requirements.

