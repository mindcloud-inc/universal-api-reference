# Pingdom: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pingdom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/get-contact?${params}`, {
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
| `contactId` | number | yes | Identifier of the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "notification_targets": {},
      "owner": true,
      "paused": true,
      "teams": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `notification_targets` | object |  |
| `owner` | boolean |  |
| `paused` | boolean |  |
| `teams` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native Pingdom API, this operation is `GET /alerting/contacts/:contactid` (base URL `https://api.pingdom.com/api/3.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

