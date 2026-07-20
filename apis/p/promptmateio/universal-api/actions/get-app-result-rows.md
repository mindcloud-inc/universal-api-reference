# Promptmate.io: Get App Result Rows



```
GET https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/get-app-result-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Promptmate.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/get-app-result-rows?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/get-app-result-rows?${params}`, {
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
| `appId` | string | yes | The Promptmate app ID whose results should be returned. |
| `jobId` | string | no | Optional Promptmate job ID to narrow the returned results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "responseFields": [
        {}
      ],
      "resultData": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string | Promptmate app ID whose results are returned. |
| `responseFields` | array<object> | Output field definitions for each result row. |
| `resultData` | array<object> | Latest Promptmate result rows for the app. |

## Native endpoint

Through the native Promptmate.io API, this operation is `GET /app-results` (base URL `https://api.promptmate.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app-result-rows.md) for the provider-specific parameters and requirements.

