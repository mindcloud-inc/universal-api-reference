# LOBSTR.IO: Get Crawler Details

Retrieves crawler details from LOBSTR.IO.

```
GET https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/get-crawler-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LOBSTR.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/get-crawler-details?connectionId=$CONNECTION_ID&crawlerHash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "crawlerHash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/get-crawler-details?${params}`, {
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
| `crawlerHash` | string | yes | The unique identifier (hash) of the crawler. |

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
      "input": [
        {}
      ],
      "isAvailable": true,
      "isPremium": true,
      "isPublic": true,
      "maxConcurrency": 1,
      "name": "Ava Chen",
      "object": "string",
      "rank": 1,
      "result": [
        "string"
      ],
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
| `input` | array<object> |  |
| `isAvailable` | boolean |  |
| `isPremium` | boolean |  |
| `isPublic` | boolean |  |
| `maxConcurrency` | number |  |
| `name` | string |  |
| `object` | string |  |
| `rank` | number |  |
| `result` | array<string> |  |
| `slug` | string |  |

## Native endpoint

Through the native LOBSTR.IO API, this operation is `GET /v1/crawlers/:crawler_hash` (base URL `https://api.lobstr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-crawler-details.md) for the provider-specific parameters and requirements.

