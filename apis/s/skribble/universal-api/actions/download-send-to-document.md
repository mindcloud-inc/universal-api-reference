# Skribble: Download Send-To Document

Retrieves the current document for a Send-To request in Skribble.

```
GET https://connect.mindcloud.co/v1/universal/skribble/latest/actions/download-send-to-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skribble/latest/actions/download-send-to-document?connectionId=$CONNECTION_ID&accessCode=string&sendToId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accessCode": "string",
  "sendToId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skribble/latest/actions/download-send-to-document?${params}`, {
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
| `accessCode` | string | yes | The Send-To access code. This will be sent as the X-Accesscode header. |
| `sendToId` | string | yes | The Send-To object ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Skribble API returns.

## Native endpoint

Through the native Skribble API, this operation is `GET /v2/sendto/:sendToId/download` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-send-to-document.md) for the provider-specific parameters and requirements.

