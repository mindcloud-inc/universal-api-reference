# SendMails: Add Subscriber Tags

Adds tags to a subscriber in SendMails.

```
PUT https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/add-subscriber-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendMails `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/add-subscriber-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/add-subscriber-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tag` | string | no | One or more tag values to add, separated by commas as documented by SendMails. |
| `uid` | string | yes | Subscriber UID from SendMails. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": 1,
      "subscriber_id": 1,
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider result message. |
| `status` | number | Provider success indicator. |
| `subscriber_id` | number | Updated subscriber numeric ID. |
| `tags` | array<string> | Subscriber tags returned after the operation. |

## Native endpoint

Through the native SendMails API, this operation is `POST /subscribers/:uid/add-tag` (base URL `https://app.sendmails.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-subscriber-tags.md) for the provider-specific parameters and requirements.

