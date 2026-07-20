# Routee: Edit planned campaign

Updates an existing planned campaign in Routee.

```
PUT https://connect.mindcloud.co/v1/universal/routee/latest/actions/edit-planned-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/routee/latest/actions/edit-planned-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/edit-planned-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | ID of the created campaign |
| `name` | string | no | Campaign name |
| `senderName` | string | no | Sender name |
| `senderEmail` | string | no | Sender email address |
| `subject` | string | no | Email subject |
| `body` | string | no | HTML code of template, encoded in base64 |
| `templateId` | string | no | ID of the template uploaded in the service. Use this method to get the template ID (use either real_id or id parameter from the reply) |
| `sendDate` | string | no | Date of the scheduled email campaign (optional parameter) must fit the following format: Y-m-d H:i:s (for example: 2016-02-02 23:34:23) and can not be less than the current date and time |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Routee API returns.

## Native endpoint

Through the native Routee API, this operation is `PATCH /campaigns` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-planned-campaign.md) for the provider-specific parameters and requirements.

