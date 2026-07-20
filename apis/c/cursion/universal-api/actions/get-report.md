# Cursion: Get Report

Retrieves an existing report from Cursion.

```
GET https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-report?connectionId=$CONNECTION_ID&reportId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reportId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-report?${params}`, {
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
| `reportId` | string | yes | The report identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "id": "string",
      "info": {},
      "page": "string",
      "path": "string",
      "site": "string",
      "time_created": "string",
      "type": [
        "string"
      ],
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `id` | string |  |
| `info` | object |  |
| `page` | string |  |
| `path` | string |  |
| `site` | string |  |
| `time_created` | string |  |
| `type` | array<string> |  |
| `user` | string |  |

## Native endpoint

Through the native Cursion API, this operation is `GET /report/{{reportId}}` (base URL `https://api.cursion.dev/v1/ops`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-report.md) for the provider-specific parameters and requirements.

