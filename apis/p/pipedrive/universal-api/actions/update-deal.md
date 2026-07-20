# Pipedrive: Update Deal

Updates an existing deal in Pipedrive.

```
PUT https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/update-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/update-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/update-deal', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currency` | string | no | Currency code, e.g. USD. |
| `expectedCloseDate` | string | no | Expected close date (YYYY-MM-DD). |
| `id` | number | yes | Unique ID of the deal to update. |
| `lostReason` | string | no | Lost reason text. |
| `status` | string | no | Deal status. |
| `title` | string | no | Deal title. |
| `ownerId` | number | no | Owner user ID. |
| `personId` | number | no | Person ID linked to deal. |
| `orgId` | number | no | Organization ID linked to deal. |
| `pipelineId` | number | no | Pipeline ID. |
| `stageId` | number | no | Stage ID. |
| `value` | number | no | Deal value. |
| `probability` | number | no | Win probability percentage. |

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

Through the native Pipedrive API, this operation is `PATCH v2/deals/:id` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-deal.md) for the provider-specific parameters and requirements.

