# Webex Interact: List contacts in list

Retrieves contacts from a list in Webex Interact.

```
GET https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/list-contacts-in-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex Interact `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/list-contacts-in-list?connectionId=$CONNECTION_ID&limit=25&offset=0&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/list-contacts-in-list?${params}`, {
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
| `fields` | string | no | Comma-separated contact fields to return. |
| `listId` | string | yes | Contact list ID whose contacts should be returned. |
| `search` | string | no | Exact phone or WhatsApp number search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "paging": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `paging` | object |  |

## Native endpoint

Through the native Webex Interact API, this operation is `GET /contacts/v1/contacts/list/{listId}` (base URL `https://api.webexinteract.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts-in-list.md) for the provider-specific parameters and requirements.

