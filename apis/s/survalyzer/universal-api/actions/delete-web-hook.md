# Survalyzer: Delete WebHook



```
DELETE https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/delete-web-hook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survalyzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/delete-web-hook?connectionId=$CONNECTION_ID&webHookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webHookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/delete-web-hook?${params}`, {
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
| `webHookId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorCode": "string",
      "errorMessage": "string",
      "isSuccess": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorCode` | string |  |
| `errorMessage` | string |  |
| `isSuccess` | boolean |  |

## Native endpoint

Through the native Survalyzer API, this operation is `POST /publicapi/WebHook/v3/DeleteWebHook` (base URL `https://api.survalyzer-eu.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-web-hook.md) for the provider-specific parameters and requirements.

