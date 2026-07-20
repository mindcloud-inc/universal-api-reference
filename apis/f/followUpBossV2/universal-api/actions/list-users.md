# Follow Up Boss: List Users

Retrieves users from Follow Up Boss.

```
GET https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Follow Up Boss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/list-users?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
      "users": [
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
| `users[]` | array<object> |  |
| `users[].acceptedShowingtimeConsent` | boolean |  |
| `users[].acceptedShowingtimeConsentV2` | boolean |  |
| `users[].beta` | boolean |  |
| `users[].canCreateApiKeys` | boolean |  |
| `users[].canExport` | boolean |  |
| `users[].created` | string |  |
| `users[].email` | string |  |
| `users[].firstName` | string |  |
| `users[].fuid` | string |  |
| `users[].groups[]` | array<object> |  |
| `users[].groups[].id` | number |  |
| `users[].groups[].name` | string |  |
| `users[].id` | number |  |
| `users[].isOwner` | boolean |  |
| `users[].lastName` | string |  |
| `users[].lastSeenAndroid` | object |  |
| `users[].lastSeenFub2` | string |  |
| `users[].lastSeenIos` | object |  |
| `users[].leadEmailAddress` | string |  |
| `users[].name` | string |  |
| `users[].pauseLeadDistribution` | boolean |  |
| `users[].phone` | string |  |
| `users[].picture` | object |  |
| `users[].picture.original` | string |  |
| `users[].picture.value162x162` | string |  |
| `users[].picture.value26x26` | string |  |
| `users[].picture.value30x30` | string |  |
| `users[].picture.value40x40` | string |  |
| `users[].picture.value60x60` | string |  |
| `users[].role` | string |  |
| `users[].status` | string |  |
| `users[].teamIds[]` | array<number> |  |
| `users[].teamLeaderOf[]` | array<string> |  |
| `users[].timezone` | string |  |
| `users[].updated` | string |  |

## Native endpoint

Through the native Follow Up Boss API, this operation is `GET users` (base URL `https://api.followupboss.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

