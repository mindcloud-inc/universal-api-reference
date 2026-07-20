# AppFollow: List Reviews

Retrieves filtered app reviews from AppFollow.

```
GET https://connect.mindcloud.co/v1/universal/appFollow/latest/actions/list-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AppFollow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appFollow/latest/actions/list-reviews?connectionId=$CONNECTION_ID&from=string&to=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "string",
  "to": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appFollow/latest/actions/list-reviews?${params}`, {
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
| `extId` | string | no | App external ID. Either ext_id or collection_name is required. |
| `collectionName` | string | no | Collection name. Either collection_name or ext_id is required. |
| `country` | string | no | Country code. |
| `lang` | string | no | Language code. |
| `reviewId` | string | no | Review ID in store. |
| `q` | string | no | Review text query. |
| `customStatus` | string | no | Custom status filter. You can filter by multiple statuses passing parameter as csv. |
| `from` | string | yes | Start date. |
| `to` | string | yes | End date. |
| `lastModified` | string | no | Review last modified filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answerDate": {},
      "answerText": {},
      "answerTime": {},
      "appVersion": {},
      "appVersionCode": {},
      "author": "string",
      "content": "string",
      "country": {},
      "created": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "device": {},
      "deviceName": {},
      "deviceType": "string",
      "hasAnswer": 1,
      "internalId": 1,
      "isAnswer": 1,
      "isDeleted": 1,
      "lang": "string",
      "langDetect": "string",
      "manufactorer": {},
      "os": {},
      "rating": 1,
      "reviewId": "string",
      "store": "string",
      "thumbsDownCnt": 1,
      "thumbsUpCnt": 1,
      "time": "string",
      "title": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "userId": {},
      "wasChanged": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answerDate` | object |  |
| `answerText` | object |  |
| `answerTime` | object |  |
| `appVersion` | object |  |
| `appVersionCode` | object |  |
| `author` | string |  |
| `content` | string |  |
| `country` | object |  |
| `created` | date |  |
| `date` | date |  |
| `device` | object |  |
| `deviceName` | object |  |
| `deviceType` | string |  |
| `hasAnswer` | number |  |
| `internalId` | number |  |
| `isAnswer` | number |  |
| `isDeleted` | number |  |
| `lang` | string |  |
| `langDetect` | string |  |
| `manufactorer` | object |  |
| `os` | object |  |
| `rating` | number |  |
| `reviewId` | string |  |
| `store` | string |  |
| `thumbsDownCnt` | number |  |
| `thumbsUpCnt` | number |  |
| `time` | string |  |
| `title` | string |  |
| `updated` | date |  |
| `userId` | object |  |
| `wasChanged` | number |  |

## Native endpoint

Through the native AppFollow API, this operation is `GET /api/v2/reviews` (base URL `https://api.appfollow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reviews.md) for the provider-specific parameters and requirements.

