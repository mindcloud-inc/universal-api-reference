# Clarifai: Get Input By ID

Retrieves an input from Clarifai.

```
GET https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/get-input-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/get-input-by-id?connectionId=$CONNECTION_ID&appId=string&inputId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string",
  "inputId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/get-input-by-id?${params}`, {
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
| `appId` | string | yes | Clarifai app ID. |
| `inputId` | string | yes | Clarifai input ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clarifai API returns.

## Native endpoint

Through the native Clarifai API, this operation is `GET /v2/users/me/apps/:appId/inputs/:inputId` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-input-by-id.md) for the provider-specific parameters and requirements.

