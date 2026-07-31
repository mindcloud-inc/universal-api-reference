# Vadivelu HTTP codes: Get GIF Status Code Image



```
GET https://connect.mindcloud.co/v1/universal/vadiveluHTTPCodes/latest/actions/get-gif-status-code-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vadivelu HTTP codes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vadiveluHTTPCodes/latest/actions/get-gif-status-code-image?connectionId=$CONNECTION_ID&statusCode=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "statusCode": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vadiveluHTTPCodes/latest/actions/get-gif-status-code-image?${params}`, {
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
| `statusCode` | list | yes | One status code with a first-party-documented GIF asset. One of: `0`, `1`, `10`, `11`, `12`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vadivelu HTTP codes API returns.

## Native endpoint

Through the native Vadivelu HTTP codes API, this operation is `GET /gif/:statusCode` (base URL `https://vadivelu.anoram.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-gif-status-code-image.md) for the provider-specific parameters and requirements.

