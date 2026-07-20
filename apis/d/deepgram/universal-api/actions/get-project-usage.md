# Deepgram: Get Project Usage

Retrieves project usage from Deepgram.

```
GET https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-project-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepgram `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-project-usage?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-project-usage?${params}`, {
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
| `start` | string | no | Start date for the requested usage range in YYYY-MM-DD format. |
| `end` | string | no | End date for the requested usage range in YYYY-MM-DD format. |
| `accessor` | string | no | Filter usage rows by accessor identifier. |
| `deployment` | string | no | Filter usage rows by deployment: hosted, beta, or self-hosted. |
| `endpoint` | string | no | Filter usage rows by endpoint: listen, read, speak, or agent. |
| `method` | string | no | Filter usage rows by method: sync, async, or streaming. |
| `model` | string | no | Filter usage rows by Deepgram model UUID. |
| `tag` | string | no | Filter usage rows by a specific tag. |

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

Through the native Deepgram API, this operation is `GET /v1/projects/:project_id/usage` (base URL `https://api.deepgram.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-usage.md) for the provider-specific parameters and requirements.

