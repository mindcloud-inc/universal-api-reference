# Follow Up Boss - Legacy: List People

Retrieves people from Follow Up Boss - Legacy.

```
GET https://connect.mindcloud.co/v1/universal/followUpBoss/latest/actions/list-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Follow Up Boss - Legacy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/followUpBoss/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/followUpBoss/latest/actions/list-people?${params}`, {
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
| `assignedLenderId` | int32 | no |  |
| `assignedLenderName` | string | no |  |
| `assignedPondId` | int32 | no |  |
| `assignedTo` | string | no |  |
| `assignedUserId` | int32 | no |  |
| `contacted` | boolean | no |  |
| `custom*` | string | no |  |
| `email` | string | no |  |
| `fields` | string | no |  |
| `firstName` | string | no |  |
| `id` | string | no |  |
| `includeTrash` | boolean | no |  |
| `includeUnclaimed` | boolean | no |  |
| `lastActivityAfter` | string | no |  |
| `lastActivityBefore` | string | no |  |
| `lastName` | string | no |  |
| `name` | string | no |  |
| `phone` | string | no |  |
| `priceAbove` | int32 | no |  |
| `priceBelow` | int32 | no |  |
| `smartListId` | int32 | no |  |
| `sort` | string | no |  |
| `source` | string | no |  |
| `stage` | string | no |  |
| `tags` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {
          "city": "string",
          "code": "string",
          "country": "string",
          "state": "string",
          "street": "string",
          "type": "string"
        }
      ],
      "assignedLenderId": {},
      "assignedLenderName": {},
      "assignedPondId": {},
      "assignedTo": "string",
      "assignedUserId": 1,
      "claimed": true,
      "collaborators": [
        {
          "assigned": true,
          "id": 1,
          "name": "Ava Chen",
          "role": "string"
        }
      ],
      "contacted": 1,
      "created": "string",
      "createdVia": "string",
      "dealCloseDate": {},
      "dealName": {},
      "dealPrice": {},
      "dealStage": {},
      "dealStatus": {},
      "delayed": true,
      "emails": [
        {
          "isPrimary": 1,
          "status": "ava@example.com",
          "type": "ava@example.com",
          "value": "ava@example.com"
        }
      ],
      "firstName": "Ava",
      "firstToClaimOffer": true,
      "id": 1,
      "lastActivity": "string",
      "lastName": "Chen",
      "leadFlowId": {},
      "name": "Ava Chen",
      "phones": [
        {
          "isLandline": true,
          "isOnboardingNumber": true,
          "isPrimary": 1,
          "normalized": "string",
          "status": "string",
          "type": "string",
          "value": "string"
        }
      ],
      "picture": {},
      "price": {},
      "source": "string",
      "sourceId": 1,
      "sourceUrl": "https://example.com",
      "stage": "string",
      "stageId": 1,
      "tags": [
        "string"
      ],
      "teamLeaders": [
        {
          "assigned": true,
          "id": 1,
          "name": "Ava Chen",
          "role": "string"
        }
      ],
      "timeframeDateRange": {},
      "timeframeId": {},
      "timeframeStatus": {},
      "timeframeUpdated": {},
      "updated": "string",
      "websiteVisits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses[].city` | string |  |
| `addresses[].code` | string |  |
| `addresses[].country` | string |  |
| `addresses[].state` | string |  |
| `addresses[].street` | string |  |
| `addresses[].type` | string |  |
| `assignedLenderId` | object |  |
| `assignedLenderName` | object |  |
| `assignedPondId` | object |  |
| `assignedTo` | string |  |
| `assignedUserId` | number |  |
| `claimed` | boolean |  |
| `collaborators[].assigned` | boolean |  |
| `collaborators[].id` | number |  |
| `collaborators[].name` | string |  |
| `collaborators[].role` | string |  |
| `contacted` | number |  |
| `created` | string |  |
| `createdVia` | string |  |
| `dealCloseDate` | object |  |
| `dealName` | object |  |
| `dealPrice` | object |  |
| `dealStage` | object |  |
| `dealStatus` | object |  |
| `delayed` | boolean |  |
| `emails[].isPrimary` | number |  |
| `emails[].status` | string |  |
| `emails[].type` | string |  |
| `emails[].value` | string |  |
| `firstName` | string |  |
| `firstToClaimOffer` | boolean |  |
| `id` | number |  |
| `lastActivity` | string |  |
| `lastName` | string |  |
| `leadFlowId` | object |  |
| `name` | string |  |
| `phones[].isLandline` | boolean |  |
| `phones[].isOnboardingNumber` | boolean |  |
| `phones[].isPrimary` | number |  |
| `phones[].normalized` | string |  |
| `phones[].status` | string |  |
| `phones[].type` | string |  |
| `phones[].value` | string |  |
| `picture` | object |  |
| `price` | object |  |
| `source` | string |  |
| `sourceId` | number |  |
| `sourceUrl` | string |  |
| `stage` | string |  |
| `stageId` | number |  |
| `tags[]` | string |  |
| `teamLeaders[].assigned` | boolean |  |
| `teamLeaders[].id` | number |  |
| `teamLeaders[].name` | string |  |
| `teamLeaders[].role` | string |  |
| `timeframeDateRange` | object |  |
| `timeframeId` | object |  |
| `timeframeStatus` | object |  |
| `timeframeUpdated` | object |  |
| `updated` | string |  |
| `websiteVisits` | number |  |

## Native endpoint

Through the native Follow Up Boss - Legacy API, this operation is `GET people` (base URL `https://api.followupboss.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-people.md) for the provider-specific parameters and requirements.

