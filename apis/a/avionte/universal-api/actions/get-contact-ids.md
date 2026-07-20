# Avionte: Get Contact IDs

Retrieves contact IDs from Avionte.

```
GET https://connect.mindcloud.co/v1/universal/avionte/latest/actions/get-contact-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avionte `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avionte/latest/actions/get-contact-ids?connectionId=$CONNECTION_ID&page=1&pageSize=50" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "page": "1",
  "pageSize": "50"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avionte/latest/actions/get-contact-ids?${params}`, {
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
| `page` | number | yes | The page number to request. Default: `1`. |
| `pageSize` | number | yes | The number of results per page. Default: `50`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avionte API returns.

## Native endpoint

Through the native Avionte API, this operation is `GET front-office/v1/contacts/ids/:page/:pageSize` (base URL `https://api.avionte.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-ids.md) for the provider-specific parameters and requirements.

