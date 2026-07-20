# TRIGGERcmd: List Commands

Retrieves a list of commands from TRIGGERcmd.

```
GET https://connect.mindcloud.co/v1/universal/tRIGGERcmd/latest/actions/list-commands
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TRIGGERcmd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tRIGGERcmd/latest/actions/list-commands?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tRIGGERcmd/latest/actions/list-commands?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TRIGGERcmd API returns.

## Native endpoint

Through the native TRIGGERcmd API, this operation is `POST /command/list` (base URL `https://www.triggercmd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-commands.md) for the provider-specific parameters and requirements.

