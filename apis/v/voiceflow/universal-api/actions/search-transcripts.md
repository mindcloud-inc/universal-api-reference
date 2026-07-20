# Voiceflow: Search Transcripts

Finds transcripts in Voiceflow by project criteria.

```
GET https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/search-transcripts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/search-transcripts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/search-transcripts?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `take` | number | no | Maximum number of results to return. Default: `25`. Example: `25`. |
| `skip` | number | no | Number of results to skip. Default: `0`. Example: `0`. |
| `order` | string | no | Sort order for returned results. Default: `DESC`. Example: `DESC`. |
| `filters[]` | array<object> | no | Filter transcripts based on properties and evaluation results. Example: `[object Object]`. |
| `endDate` | string | no | Only include transcripts started before this timestamp. Example: `2026-03-26T00:00:00Z`. |
| `sessionId` | string | no | Only include transcripts for this session. Example: `mindcloud-vf-interact-user-001`. |
| `startDate` | string | no | Only include transcripts started after this timestamp. Example: `2026-03-01T00:00:00Z`. |
| `environmentId` | string | no | Only include transcripts for this environment. Example: `development`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Voiceflow API returns.

## Native endpoint

Through the native Voiceflow API, this operation is `POST https://analytics-api.voiceflow.com/v1/transcript/project/:projectId` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-transcripts.md) for the provider-specific parameters and requirements.

