# Pipedrive: Get Deal

Retrieves a deal from Pipedrive.

```
GET https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-deal?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-deal?${params}`, {
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
| `customFields` | string | no | Comma-separated custom field hashes to include. |
| `id` | number | yes | Unique ID of the deal. |
| `includeFields` | string | no | Comma-separated additional fields to include. |

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

Through the native Pipedrive API, this operation is `GET v2/deals/:id` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deal.md) for the provider-specific parameters and requirements.

