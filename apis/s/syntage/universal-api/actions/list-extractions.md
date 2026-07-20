# Syntage: List Extractions

Retrieves extractions from Syntage.

```
GET https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-extractions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syntage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-extractions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-extractions?${params}`, {
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
      "@id": "string",
      "@type": "string",
      "createdAt": "string",
      "createdDataPoints": 1,
      "errorCode": "string",
      "extractor": "string",
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "options": {},
      "rateLimitedAt": "2026-05-07T12:00:00.000Z",
      "startedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "taxpayer": {},
      "updatedAt": "string",
      "updatedDataPoints": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@id` | string |  |
| `@type` | string |  |
| `createdAt` | string |  |
| `createdDataPoints` | number |  |
| `errorCode` | string |  |
| `extractor` | string |  |
| `finishedAt` | date |  |
| `id` | string |  |
| `options` | object |  |
| `rateLimitedAt` | date |  |
| `startedAt` | date |  |
| `status` | string |  |
| `taxpayer` | object |  |
| `updatedAt` | string |  |
| `updatedDataPoints` | number |  |

## Native endpoint

Through the native Syntage API, this operation is `GET /extractions` (base URL `https://api.sandbox.syntage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-extractions.md) for the provider-specific parameters and requirements.

