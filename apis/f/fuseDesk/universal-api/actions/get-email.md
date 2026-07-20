# FuseDesk: Get Email

Retrieves an email record from FuseDesk.

```
GET https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/get-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FuseDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/get-email?connectionId=$CONNECTION_ID&emailId=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailId": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/get-email?${params}`, {
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
| `emailId` | string | yes | The FuseDesk email ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FuseDesk API returns.

## Native endpoint

Through the native FuseDesk API, this operation is `GET /api/v1/emails/:emailId` (base URL `https://{{credentials.appName}}.fusedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email.md) for the provider-specific parameters and requirements.

