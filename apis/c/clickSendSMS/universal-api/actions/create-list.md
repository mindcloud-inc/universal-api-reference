# ClickSend SMS: Create List

Creates a new contact list in ClickSend SMS.

```
POST https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/create-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/create-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/create-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listName` | string | yes | Name for the contact list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactsCount": 1,
      "importInProgress": 1,
      "listEmailId": "ava@example.com",
      "listId": 1,
      "listName": "Ava Chen",
      "optoutInProgress": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactsCount` | number |  |
| `importInProgress` | number |  |
| `listEmailId` | string |  |
| `listId` | number |  |
| `listName` | string |  |
| `optoutInProgress` | number |  |

## Native endpoint

Through the native ClickSend SMS API, this operation is `POST /v3/lists` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list.md) for the provider-specific parameters and requirements.

