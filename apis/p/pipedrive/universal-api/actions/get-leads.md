# Pipedrive: Get Leads

Retrieves leads from Pipedrive.

```
GET https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-leads?${params}`, {
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
| `limit` | number | no | Max number of leads to return. |
| `start` | number | no | Offset for lead pagination. |
| `updatedSince` | string | no | Return leads updated after this timestamp. |
| `sort` | string | no | Sort leads by a timestamp field and direction. |
| `ownerId` | number | no | Filter leads by owner user ID. |

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

Through the native Pipedrive API, this operation is `GET v1/leads` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-leads.md) for the provider-specific parameters and requirements.

