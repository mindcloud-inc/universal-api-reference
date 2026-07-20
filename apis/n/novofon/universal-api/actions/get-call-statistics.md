# Novofon: Get Call Statistics

Retrieves call statistics from Novofon.

```
GET https://connect.mindcloud.co/v1/universal/novofon/latest/actions/get-call-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novofon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/novofon/latest/actions/get-call-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/novofon/latest/actions/get-call-statistics?${params}`, {
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
| `costOnly` | string | no | Optional provider flag to return only spent cost for the selected period. |
| `end` | string | no | Optional statistics window end in `YYYY-MM-DD HH:MM:SS` format. |
| `limit` | string | no | Optional maximum number of rows to return. Docs say the provider maximum is 1000. |
| `sip` | string | no | Optional SIP number filter. |
| `skip` | string | no | Optional number of rows to skip for pagination. |
| `start` | string | no | Optional statistics window start in `YYYY-MM-DD HH:MM:SS` format. |
| `type` | string | no | Optional provider statistics type such as `toll` or `ru495`. Leave empty for the default overall statistics. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end": "2026-05-07T12:00:00.000Z",
      "start": "2026-05-07T12:00:00.000Z",
      "stats": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end` | date |  |
| `start` | date |  |
| `stats` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native Novofon API, this operation is `GET /v1/statistics/` (base URL `https://api.novofon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-statistics.md) for the provider-specific parameters and requirements.

