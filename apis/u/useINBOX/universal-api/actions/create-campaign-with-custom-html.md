# UseINBOX: Create Campaign With Custom HTML

Creates a campaign from custom HTML in UseINBOX.

```
POST https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/create-campaign-with-custom-html
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UseINBOX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/create-campaign-with-custom-html" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "senderAccountId": "string",
  "listType": 1,
  "lists[]": [
    "string"
  ],
  "subject": "string",
  "htmlContent": "string",
  "language": "en-US"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/create-campaign-with-custom-html', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "senderAccountId": "string",
    "listType": 1,
    "lists[]": ["string"],
    "subject": "string",
    "htmlContent": "string",
    "language": "en-US"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `senderAccountId` | string | yes | Sender account ID used for the campaign. |
| `listType` | number | yes | INBOX list type value for the campaign audience. |
| `lists[]` | array<string> | yes | Contact list IDs that should receive the campaign. Accepts multiple values as an array. |
| `subject` | string | yes | Subject line for the custom HTML campaign. |
| `htmlContent` | string | yes | HTML content for the campaign. |
| `language` | string | yes | Campaign language code such as en-US. Default: `en-US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "plannedTime": "2026-05-07T12:00:00.000Z",
      "status": 1,
      "subject": "string",
      "updateTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTime` | date |  |
| `id` | string |  |
| `plannedTime` | date |  |
| `status` | number |  |
| `subject` | string |  |
| `updateTime` | date |  |

## Native endpoint

Through the native UseINBOX API, this operation is `POST /inbox/v1/campaigns/custom` (base URL `https://useapi.useinbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign-with-custom-html.md) for the provider-specific parameters and requirements.

