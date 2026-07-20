# Novofon: Get PBX Call Statistics

Retrieves PBX call statistics from Novofon.

```
GET https://connect.mindcloud.co/v1/universal/novofon/latest/actions/get-pbx-call-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novofon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/novofon/latest/actions/get-pbx-call-statistics?connectionId=$CONNECTION_ID&version=2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "version": "2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/novofon/latest/actions/get-pbx-call-statistics?${params}`, {
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
| `callType` | string | no | Optional call direction filter. Docs list `in` for inbound and `out` for outbound. |
| `end` | string | no | Optional statistics window end in `YYYY-MM-DD HH:MM:SS` format. |
| `limit` | string | no | Optional maximum number of rows to return. Docs say the provider maximum is 1000. |
| `skip` | string | no | Optional number of rows to skip for pagination. |
| `start` | string | no | Optional statistics window start in `YYYY-MM-DD HH:MM:SS` format. |
| `version` | string | yes | PBX statistics response format version. Docs list `2` as the new format and `1` as the old format. Default: `2`. |

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
      "status": "string",
      "version": 1
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
| `version` | number |  |

## Native endpoint

Through the native Novofon API, this operation is `GET /v1/statistics/pbx/` (base URL `https://api.novofon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pbx-call-statistics.md) for the provider-specific parameters and requirements.

