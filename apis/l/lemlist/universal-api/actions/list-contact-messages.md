# lemlist: List Contact Messages

Retrieves contact messages from lemlist inbox.

```
GET https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/list-contact-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lemlist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/list-contact-messages?connectionId=$CONNECTION_ID&contactId=ctc_yHXD3NWjPg7Z9MuWZ" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "ctc_yHXD3NWjPg7Z9MuWZ"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/list-contact-messages?${params}`, {
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
| `contactId` | string | yes | The unique identifier of the contact. Example: `ctc_yHXD3NWjPg7Z9MuWZ`. |
| `userId` | string | no | Required when `markAsRead` is provided so lemlist can resolve the viewing user. Example: `usr_vvv9vehz2Ghvgbedv`. |
| `skip` | number | no | Number of items to skip. Example: `0`. |
| `markAsRead` | boolean | no | When true, marks the conversation as read. If provided, also send `userId`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "attachments": [
            "string"
          ],
          "campaignId": "string",
          "contactId": "string",
          "createdAt": "string",
          "fromEmail": "ava@example.com",
          "id": "string",
          "leadEmail": "ava@example.com",
          "leadFirstName": "Ava",
          "leadId": "string",
          "leadLastName": "Chen",
          "message": "string",
          "messageId": "string",
          "sendUserEmail": "ava@example.com",
          "sendUserId": "string",
          "sendUserMailboxId": "string",
          "sendUserName": "Ava Chen",
          "subject": "string",
          "teamId": "string",
          "type": "string"
        }
      ],
      "pagination": {
        "currentPage": 1,
        "nextPage": "string",
        "perPage": 1,
        "previousPage": "string",
        "totalItems": 1,
        "totalPages": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].attachments` | array<string> |  |
| `data[].campaignId` | string |  |
| `data[].contactId` | string |  |
| `data[].createdAt` | string |  |
| `data[].fromEmail` | string |  |
| `data[].id` | string |  |
| `data[].leadEmail` | string |  |
| `data[].leadFirstName` | string |  |
| `data[].leadId` | string |  |
| `data[].leadLastName` | string |  |
| `data[].message` | string |  |
| `data[].messageId` | string |  |
| `data[].sendUserEmail` | string |  |
| `data[].sendUserId` | string |  |
| `data[].sendUserMailboxId` | string |  |
| `data[].sendUserName` | string |  |
| `data[].subject` | string |  |
| `data[].teamId` | string |  |
| `data[].type` | string |  |
| `pagination` | object |  |
| `pagination.currentPage` | number |  |
| `pagination.nextPage` | string |  |
| `pagination.perPage` | number |  |
| `pagination.previousPage` | string |  |
| `pagination.totalItems` | number |  |
| `pagination.totalPages` | number |  |

## Native endpoint

Through the native lemlist API, this operation is `GET /inbox/:contactId` (base URL `https://api.lemlist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-messages.md) for the provider-specific parameters and requirements.

