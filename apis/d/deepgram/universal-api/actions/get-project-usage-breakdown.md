# Deepgram: Get Project Usage Breakdown

Retrieves a project usage breakdown from Deepgram.

```
GET https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-project-usage-breakdown
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepgram `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-project-usage-breakdown?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-project-usage-breakdown?${params}`, {
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
| `projectId` | string | yes | Deepgram project identifier. |
| `start` | string | no | Start date for the requested usage-breakdown range in YYYY-MM-DD format. |
| `end` | string | no | End date for the requested usage-breakdown range in YYYY-MM-DD format. |
| `grouping` | string | no | Usage grouping dimension from the Deepgram reference. |
| `accessor` | string | no | Filter usage breakdown rows by accessor identifier. |
| `deployment` | string | no | Filter usage breakdown rows by deployment: hosted, beta, or self-hosted. |
| `endpoint` | string | no | Filter usage breakdown rows by endpoint: listen, read, speak, or agent. |
| `method` | string | no | Filter usage breakdown rows by method: sync, async, or streaming. |
| `model` | string | no | Filter usage breakdown rows by Deepgram model UUID. |
| `tag` | string | no | Filter usage breakdown rows by a specific tag. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end": "string",
      "resolution": {},
      "results": [
        {}
      ],
      "start": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end` | string |  |
| `resolution` | object |  |
| `results` | array<object> |  |
| `start` | string |  |

## Native endpoint

Through the native Deepgram API, this operation is `GET /v1/projects/:project_id/usage/breakdown` (base URL `https://api.deepgram.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-usage-breakdown.md) for the provider-specific parameters and requirements.

