# Docutray: Get Step Execution Status



```
GET https://connect.mindcloud.co/v1/universal/docutray/latest/actions/get-step-execution-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docutray `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docutray/latest/actions/get-step-execution-status?connectionId=$CONNECTION_ID&executionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "executionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docutray/latest/actions/get-step-execution-status?${params}`, {
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
| `executionId` | string | yes | Step execution ID returned from the execute step endpoint |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Docutray API returns.

## Native endpoint

Through the native Docutray API, this operation is `GET api/steps-async/status/:executionId` (base URL `https://app.docutray.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-step-execution-status.md) for the provider-specific parameters and requirements.

