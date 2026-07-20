# Brevo: Remove Contacts from List



```
DELETE https://connect.mindcloud.co/v1/universal/brevo/latest/actions/remove-contacts-from-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/remove-contacts-from-list?connectionId=$CONNECTION_ID&emails=%5Bobject%20Object%5D&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emails": "[object Object]",
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/remove-contacts-from-list?${params}`, {
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
| `emails` | object<string> | yes | Array of contact emails to remove from the list. |
| `listId` | string | yes | Brevo list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": {
        "failure": [
          "string"
        ],
        "success": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts.failure` | array |  |
| `contacts.success` | array<string> |  |

## Native endpoint

Through the native Brevo API, this operation is `POST /v3/contacts/lists/:listId/contacts/remove` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-contacts-from-list.md) for the provider-specific parameters and requirements.

