# Pipedrive: List Deals

Retrieves deals from Pipedrive.

```
GET https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/list-deals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/list-deals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/list-deals?${params}`, {
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
| `status` | string | no | Filter by deal status: open, won, lost, deleted, or all_not_deleted. |
| `sortBy` | string | no | Sort field for returned deals. |
| `sortDirection` | string | no | Sort direction: asc or desc. |
| `updatedSince` | string | no | Return deals updated after this timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addTime": "string",
      "archiveTime": {},
      "channel": 1,
      "channelId": "string",
      "closeTime": {},
      "creatorUserId": 1,
      "currency": "string",
      "customFields": {},
      "expectedCloseDate": {},
      "id": 1,
      "isArchived": true,
      "isDeleted": true,
      "localCloseDate": {},
      "localLostDate": {},
      "localWonDate": {},
      "lostReason": {},
      "lostTime": {},
      "orgId": {},
      "origin": "string",
      "originId": "string",
      "ownerId": 1,
      "personId": {},
      "pipelineId": 1,
      "probability": {},
      "stageChangeTime": {},
      "stageId": 1,
      "status": "string",
      "title": "string",
      "updateTime": "string",
      "value": 1,
      "visibleTo": 1,
      "wonTime": {}
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
| `channel` | number |  |
| `channelId` | string |  |
| `closeTime` | object |  |
| `creatorUserId` | number |  |
| `currency` | string |  |
| `customFields` | object |  |
| `expectedCloseDate` | object |  |
| `id` | number |  |
| `isArchived` | boolean |  |
| `isDeleted` | boolean |  |
| `localCloseDate` | object |  |
| `localLostDate` | object |  |
| `localWonDate` | object |  |
| `lostReason` | object |  |
| `lostTime` | object |  |
| `orgId` | object |  |
| `origin` | string |  |
| `originId` | string |  |
| `ownerId` | number |  |
| `personId` | object |  |
| `pipelineId` | number |  |
| `probability` | object |  |
| `stageChangeTime` | object |  |
| `stageId` | number |  |
| `status` | string |  |
| `title` | string |  |
| `updateTime` | string |  |
| `value` | number |  |
| `visibleTo` | number |  |
| `wonTime` | object |  |

## Native endpoint

Through the native Pipedrive API, this operation is `GET v2/deals` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-deals.md) for the provider-specific parameters and requirements.

