# SendMails: Add List Field

Adds a custom field to a list in SendMails.

```
POST https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/add-list-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendMails `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/add-list-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uid": "string",
  "type": "string",
  "label": "string",
  "tag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/add-list-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uid": "string",
    "type": "string",
    "label": "string",
    "tag": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uid` | string | yes | List UID from SendMails. |
| `type` | string | yes | Custom-field type: text, number, or datetime. |
| `label` | string | yes | Field label. |
| `tag` | string | yes | Field tag name using alphanumeric characters, dashes, or underscores. |
| `defaultValue` | string | no | Optional default value for the custom field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field": {},
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field` | object | Created list field definition. |
| `message` | string | Provider result message. |
| `status` | number | Provider success indicator. |

## Native endpoint

Through the native SendMails API, this operation is `POST /lists/:uid/add-field` (base URL `https://app.sendmails.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-list-field.md) for the provider-specific parameters and requirements.

