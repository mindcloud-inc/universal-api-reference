# OnlineCheckWriter: List Mail Check Mailing Options

Lists available mailing, paper, and insert options for mail checks.

```
GET https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/list-mail-check-mailing-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnlineCheckWriter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/list-mail-check-mailing-options?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/list-mail-check-mailing-options?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OnlineCheckWriter API returns.

## Native endpoint

Through the native OnlineCheckWriter API, this operation is `GET /mailchecks/mailingOptions` (base URL `https://test.onlinecheckwriter.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mail-check-mailing-options.md) for the provider-specific parameters and requirements.

