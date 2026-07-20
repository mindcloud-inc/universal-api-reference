# Wooxy: List Contact Lists

Finds contact lists in your Wooxy account.

```
GET https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/list-contact-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/list-contact-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/list-contact-lists?${params}`, {
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
| `contactListId` | string | no | Contact list ID in Wooxy. |
| `contactListName` | string | no | Contact list name in Wooxy. |
| `domain` | string | no | Verified sender domain in Wooxy. |
| `domainId` | string | no | Unique Wooxy domain ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "limit": 1,
      "offset": 1,
      "result": true,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limit` | number |  |
| `offset` | number |  |
| `result` | boolean |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/contact-list/find` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contact-lists.md) for the provider-specific parameters and requirements.

