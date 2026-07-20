# Pipedrive: Add Lead

Creates a new lead in Pipedrive.

```
POST https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/add-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/add-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadTitle": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/add-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leadTitle": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leadTitle` | string | yes | Lead title. |
| `personId` | number | no | Person ID to link to the lead. |
| `organizationId` | number | no | Organization ID to link to the lead. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addTime": "string",
      "archiveTime": {},
      "ccEmail": "ava@example.com",
      "channel": 1,
      "channelId": "string",
      "creatorId": 1,
      "expectedCloseDate": {},
      "id": "string",
      "isArchived": true,
      "nextActivityId": {},
      "organizationId": 1,
      "origin": "string",
      "originId": "string",
      "ownerId": 1,
      "personId": {},
      "sourceDealId": {},
      "sourceName": "Ava Chen",
      "title": "string",
      "updateTime": "string",
      "value": {},
      "visibleTo": "string",
      "wasSeen": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addTime` | string |  |
| `archiveTime` | object |  |
| `ccEmail` | string |  |
| `channel` | number |  |
| `channelId` | string |  |
| `creatorId` | number |  |
| `expectedCloseDate` | object |  |
| `id` | string |  |
| `isArchived` | boolean |  |
| `nextActivityId` | object |  |
| `organizationId` | number |  |
| `origin` | string |  |
| `originId` | string |  |
| `ownerId` | number |  |
| `personId` | object |  |
| `sourceDealId` | object |  |
| `sourceName` | string |  |
| `title` | string |  |
| `updateTime` | string |  |
| `value` | object |  |
| `visibleTo` | string |  |
| `wasSeen` | boolean |  |

## Native endpoint

Through the native Pipedrive API, this operation is `POST v1/leads` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-lead.md) for the provider-specific parameters and requirements.

