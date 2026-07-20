# Sendible: Get TikTok Report



```
GET https://connect.mindcloud.co/v1/universal/sendible/latest/actions/get-tik-tok-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendible `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendible/latest/actions/get-tik-tok-report?connectionId=$CONNECTION_ID&accountId=1&end=string&module=string&start=string&timezoneOffset=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "end": "string",
  "module": "string",
  "start": "string",
  "timezoneOffset": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendible/latest/actions/get-tik-tok-report?${params}`, {
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
| `accountId` | number | yes | TikTok account ID. |
| `end` | string | yes | Report end date. |
| `module` | string | yes | TikTok report module, such as ActivityOverview or Audience. |
| `start` | string | yes | Report start date. |
| `timezoneOffset` | number | yes | Timezone offset in minutes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |

## Native endpoint

Through the native Sendible API, this operation is `GET 0.2/tw/tiktok/report` (base URL `https://api.sendible.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tik-tok-report.md) for the provider-specific parameters and requirements.

