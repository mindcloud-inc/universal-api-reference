# Bannertize: Get Template

Retrieves a template and its modifications from Bannertize.

```
GET https://connect.mindcloud.co/v1/universal/bannertize/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bannertize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bannertize/latest/actions/get-template?connectionId=$CONNECTION_ID&template_uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "template_uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bannertize/latest/actions/get-template?${params}`, {
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
| `template_uid` | string | yes | The Bannertize template UID to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bannertize API returns.

## Native endpoint

Through the native Bannertize API, this operation is `GET template/:template_uid` (base URL `https://api.bannertize.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

