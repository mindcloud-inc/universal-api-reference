# ClickSend SMS: List Contact Lists

Retrieves contact lists from ClickSend SMS.

```
GET https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/list-contact-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/list-contact-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/list-contact-lists?${params}`, {
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
| `page` | number | no | Page number. |
| `limit` | number | no | Items per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
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
      "from": 1,
      "lastPage": 1,
      "nextPageUrl": {},
      "perPage": 1,
      "prevPageUrl": {},
      "to": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number |  |
| `data[].contactsCount` | number |  |
| `data[].importInProgress` | number |  |
| `data[].listEmailId` | string |  |
| `data[].listId` | number |  |
| `data[].listName` | string |  |
| `data[].optoutInProgress` | number |  |
| `from` | number |  |
| `lastPage` | number |  |
| `nextPageUrl` | object |  |
| `perPage` | number |  |
| `prevPageUrl` | object |  |
| `to` | number |  |
| `total` | number |  |

## Native endpoint

Through the native ClickSend SMS API, this operation is `GET /v3/lists` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contact-lists.md) for the provider-specific parameters and requirements.

