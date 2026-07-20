# Follow Up Boss: List People

Retrieves people from Follow Up Boss.

```
GET https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/list-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Follow Up Boss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/list-people?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/list-people?${params}`, {
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
| `id` | string | no |  |
| `name` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `email` | string | no |  |
| `phone` | string | no |  |
| `stage` | string | no |  |
| `source` | string | no |  |
| `assignedTo` | string | no |  |
| `assignedUserId` | number | no |  |
| `assignedPondId` | number | no |  |
| `assignedLenderName` | string | no |  |
| `assignedLenderId` | number | no |  |
| `contacted` | boolean | no |  |
| `priceAbove` | number | no |  |
| `priceBelow` | number | no |  |
| `smartListId` | number | no |  |
| `tags` | string | no |  |
| `lastActivityAfter` | string | no |  |
| `lastActivityBefore` | string | no |  |
| `sort` | string | no |  |
| `fields` | string | no |  |
| `includeTrash` | boolean | no |  |
| `includeUnclaimed` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {
        "collection": "string",
        "limit": 1,
        "next": {},
        "nextLink": {},
        "offset": 1,
        "total": 1
      },
      "people": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata` | object |  |
| `metadata.collection` | string |  |
| `metadata.limit` | number |  |
| `metadata.next` | object |  |
| `metadata.nextLink` | object |  |
| `metadata.offset` | number |  |
| `metadata.total` | number |  |
| `people[]` | array<object> |  |
| `people[].addresses[]` | array<string> |  |
| `people[].assignedLenderId` | object |  |
| `people[].assignedLenderName` | object |  |
| `people[].assignedPondId` | object |  |
| `people[].assignedTo` | string |  |
| `people[].assignedUserId` | number |  |
| `people[].claimed` | boolean |  |
| `people[].collaborators[]` | array<object> |  |
| `people[].collaborators[].assigned` | boolean |  |
| `people[].collaborators[].id` | number |  |
| `people[].collaborators[].name` | string |  |
| `people[].collaborators[].role` | string |  |
| `people[].contacted` | number |  |
| `people[].created` | string |  |
| `people[].createdVia` | object |  |
| `people[].dealCloseDate` | string |  |
| `people[].dealName` | string |  |
| `people[].dealPrice` | number |  |
| `people[].dealStage` | string |  |
| `people[].dealStatus` | string |  |
| `people[].delayed` | boolean |  |
| `people[].emails[]` | array<object> |  |
| `people[].emails[].isPrimary` | number |  |
| `people[].emails[].status` | string |  |
| `people[].emails[].type` | string |  |
| `people[].emails[].value` | string |  |
| `people[].firstName` | string |  |
| `people[].firstToClaimOffer` | boolean |  |
| `people[].id` | number |  |
| `people[].lastActivity` | string |  |
| `people[].lastName` | string |  |
| `people[].leadFlowId` | object |  |
| `people[].name` | string |  |
| `people[].phones[]` | array<object> |  |
| `people[].phones[].isLandline` | boolean |  |
| `people[].phones[].isOnboardingNumber` | boolean |  |
| `people[].phones[].isPrimary` | number |  |
| `people[].phones[].normalized` | string |  |
| `people[].phones[].status` | string |  |
| `people[].phones[].type` | string |  |
| `people[].phones[].value` | string |  |
| `people[].picture` | object |  |
| `people[].picture.small` | string |  |
| `people[].pondMembers[]` | array<string> |  |
| `people[].price` | object |  |
| `people[].socialData` | object |  |
| `people[].socialData.age` | string |  |
| `people[].socialData.bio` | string |  |
| `people[].socialData.company` | string |  |
| `people[].socialData.facebook` | string |  |
| `people[].socialData.firstName` | string |  |
| `people[].socialData.gender` | string |  |
| `people[].socialData.googlePlus` | string |  |
| `people[].socialData.googleProfile` | string |  |
| `people[].socialData.lastName` | string |  |
| `people[].socialData.linkedIn` | string |  |
| `people[].socialData.location` | string |  |
| `people[].socialData.name` | string |  |
| `people[].socialData.title` | string |  |
| `people[].socialData.topics` | string |  |
| `people[].socialData.twitter` | string |  |
| `people[].source` | string |  |
| `people[].sourceId` | number |  |
| `people[].sourceUrl` | string |  |
| `people[].stage` | string |  |
| `people[].stageId` | number |  |
| `people[].tags[]` | array<string> |  |
| `people[].teamLeaders[]` | array<string> |  |
| `people[].timeframeDateRange` | string |  |
| `people[].timeframeId` | number |  |
| `people[].timeframeStatus` | string |  |
| `people[].timeframeUpdated` | string |  |
| `people[].type` | string |  |
| `people[].updated` | string |  |
| `people[].websiteVisits` | number |  |

## Native endpoint

Through the native Follow Up Boss API, this operation is `GET people` (base URL `https://api.followupboss.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-people.md) for the provider-specific parameters and requirements.

