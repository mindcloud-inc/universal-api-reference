# Apollo: Get Lists and Tags

Retrieves information about all lists and tags in your Apollo account. This action can be used to check available lists before using the Create a Contact action.

```
GET https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/get-a-list-of-all-lists-and-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/get-a-list-of-all-lists-and-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/get-a-list-of-all-lists-and-tags?${params}`, {
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
      "cachedCount": 1,
      "concurrencyLocks": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "Id": "string",
      "key": "string",
      "modality": "string",
      "name": "Ava Chen",
      "needCachedCountUpdate": {},
      "needsCountUpdateAt": {},
      "ruleConfigTemplateId": {},
      "teamId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cachedCount` | number |  |
| `concurrencyLocks` | object |  |
| `createdAt` | date |  |
| `id` | string |  |
| `Id` | string |  |
| `key` | string |  |
| `modality` | string |  |
| `name` | string |  |
| `needCachedCountUpdate` | object |  |
| `needsCountUpdateAt` | object |  |
| `ruleConfigTemplateId` | object |  |
| `teamId` | string |  |
| `updatedAt` | date |  |
| `userId` | string |  |

## Native endpoint

Through the native Apollo API, this operation is `GET v1/labels` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-list-of-all-lists-and-tags.md) for the provider-specific parameters and requirements.

