# Telldus Live!: List Rooms

Retrieves your rooms from Telldus Live!.

```
GET https://connect.mindcloud.co/v1/universal/telldusLive/latest/actions/list-rooms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Telldus Live! `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/telldusLive/latest/actions/list-rooms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/telldusLive/latest/actions/list-rooms?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Telldus Live! API returns.

## Native endpoint

Through the native Telldus Live! API, this operation is `GET /json/rooms/list` (base URL `https://pa-api.telldus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-rooms.md) for the provider-specific parameters and requirements.

