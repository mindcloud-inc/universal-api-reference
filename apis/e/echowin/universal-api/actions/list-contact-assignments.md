# echowin: List Contact Assignments

Retrieves contact assignments from echowin.

```
GET https://connect.mindcloud.co/v1/universal/echowin/latest/actions/list-contact-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a echowin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/echowin/latest/actions/list-contact-assignments?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/echowin/latest/actions/list-contact-assignments?${params}`, {
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
| `contactId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native echowin API returns.

## Native endpoint

Through the native echowin API, this operation is `GET /contacts/:contactId/assignments` (base URL `https://echo.win/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-assignments.md) for the provider-specific parameters and requirements.

