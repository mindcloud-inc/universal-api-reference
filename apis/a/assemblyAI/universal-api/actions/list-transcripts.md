# AssemblyAI: List Transcripts

Retrieves transcript records from your AssemblyAI account.

```
GET https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/list-transcripts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssemblyAI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/list-transcripts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/list-transcripts?${params}`, {
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
| `limit` | number | no | Maximum number of transcripts to retrieve. Default: `10`. |
| `status` | string | no | Filter transcripts by status. |
| `createdOn` | date | no | Only return transcripts created on this date. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `beforeId` | string | no | Return transcripts created before this transcript ID. |
| `afterId` | string | no | Return transcripts created after this transcript ID. |
| `throttledOnly` | boolean | no | Only return throttled transcripts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pageDetails": {
        "currentUrl": "https://example.com",
        "limit": 1,
        "nextUrl": "https://example.com",
        "prevUrl": "https://example.com",
        "resultCount": 1
      },
      "transcripts": [
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
| `pageDetails` | object |  |
| `pageDetails.currentUrl` | string |  |
| `pageDetails.limit` | number |  |
| `pageDetails.nextUrl` | string |  |
| `pageDetails.prevUrl` | string |  |
| `pageDetails.resultCount` | number |  |
| `transcripts[]` | array<object> |  |
| `transcripts[].audioUrl` | string |  |
| `transcripts[].completed` | date |  |
| `transcripts[].created` | date |  |
| `transcripts[].error` | string |  |
| `transcripts[].id` | string |  |
| `transcripts[].region` | object |  |
| `transcripts[].resourceUrl` | string |  |
| `transcripts[].status` | string |  |

## Native endpoint

Through the native AssemblyAI API, this operation is `GET /v2/transcript` (base URL `https://api.assemblyai.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transcripts.md) for the provider-specific parameters and requirements.

