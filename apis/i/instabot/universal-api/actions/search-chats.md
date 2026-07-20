# Instabot: Search Chats

Finds chats in Instabot by search filters.

```
GET https://connect.mindcloud.co/v1/universal/instabot/latest/actions/search-chats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instabot `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instabot/latest/actions/search-chats?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instabot/latest/actions/search-chats?${params}`, {
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
| `searchString` | string | no | Text used to search chats. |
| `startDate` | date | no | Start of the chat search date window. |
| `endDate` | date | no | End of the chat search date window. |
| `botDeletionStatus` | string | no | Filter chats by bot deletion status. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Instabot API returns.

## Native endpoint

Through the native Instabot API, this operation is `POST /instabot/chats/search` (base URL `https://api.instabot.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-chats.md) for the provider-specific parameters and requirements.

