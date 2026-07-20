# Skribble: Create Send-To

Creates a Send-To signing request in Skribble.

```
POST https://connect.mindcloud.co/v1/universal/skribble/latest/actions/create-send-to
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/skribble/latest/actions/create-send-to" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skribble/latest/actions/create-send-to', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | The base64 encoded PDF content. |
| `title` | string | no | The Send-To title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_code": "string",
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_code` | string | The access code required for follow-up Send-To actions. |
| `id` | string | The Send-To object ID. |
| `url` | string | The Send-To URL to share. |

## Native endpoint

Through the native Skribble API, this operation is `POST /v2/sendto` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-send-to.md) for the provider-specific parameters and requirements.

