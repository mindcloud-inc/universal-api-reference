# LOBSTR.IO: List Crawlers

Retrieves crawlers from LOBSTR.IO.

```
GET https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/list-crawlers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LOBSTR.IO `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/list-crawlers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/list-crawlers?${params}`, {
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
      "account": {},
      "creditsPerEmail": {},
      "creditsPerRow": {},
      "defaultWorkerStats": {},
      "description": "string",
      "emailWorkerStats": {},
      "hasEmailVerification": true,
      "hasIssues": true,
      "icon": "string",
      "id": "string",
      "isAvailable": true,
      "isPremium": true,
      "isPublic": true,
      "maxConcurrency": 1,
      "name": "Ava Chen",
      "object": "string",
      "rank": 1,
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `creditsPerEmail` | object |  |
| `creditsPerRow` | object |  |
| `defaultWorkerStats` | object |  |
| `description` | string |  |
| `emailWorkerStats` | object |  |
| `hasEmailVerification` | boolean |  |
| `hasIssues` | boolean |  |
| `icon` | string |  |
| `id` | string |  |
| `isAvailable` | boolean |  |
| `isPremium` | boolean |  |
| `isPublic` | boolean |  |
| `maxConcurrency` | number |  |
| `name` | string |  |
| `object` | string |  |
| `rank` | number |  |
| `slug` | string |  |

## Native endpoint

Through the native LOBSTR.IO API, this operation is `GET /v1/crawlers` (base URL `https://api.lobstr.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-crawlers.md) for the provider-specific parameters and requirements.

