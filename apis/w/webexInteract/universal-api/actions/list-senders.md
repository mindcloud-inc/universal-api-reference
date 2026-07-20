# Webex Interact: List senders

Retrieves senders from Webex Interact.

```
GET https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/list-senders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex Interact `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/list-senders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/list-senders?${params}`, {
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
| `page_number` | string | no | Page number to return. Defaults to 1. |
| `page_size` | string | no | Number of senders per page. Defaults to 25. Maximum 100. |

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

Through the native Webex Interact API, this operation is `GET /assets/v1/senders` (base URL `https://api.webexinteract.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-senders.md) for the provider-specific parameters and requirements.

