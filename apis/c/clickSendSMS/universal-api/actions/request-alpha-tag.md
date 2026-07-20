# ClickSend SMS: Request Alpha Tag

Requests a new alpha tag in ClickSend SMS.

```
POST https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/request-alpha-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/request-alpha-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "alphaTag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/request-alpha-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "alphaTag": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `alphaTag` | string | yes | Requested alpha sender tag. |
| `reason` | string | no | Business reason for requesting the tag. |
| `countries[]` | array<string> | no | ISO country codes where the tag will be used. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businesses[]` | array<object> | no | Business metadata objects for approval. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "alphaTag": "string",
      "countries": [
        "string"
      ],
      "createdTimestamp": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "reason": "string",
      "status": "string",
      "updatedTimestamp": "2026-05-07T12:00:00.000Z",
      "userId": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `alphaTag` | string |  |
| `countries` | array<string> |  |
| `createdTimestamp` | date |  |
| `id` | string |  |
| `reason` | string |  |
| `status` | string |  |
| `updatedTimestamp` | date |  |
| `userId` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native ClickSend SMS API, this operation is `POST /v3/alpha-tags` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-alpha-tag.md) for the provider-specific parameters and requirements.

