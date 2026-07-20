# Persona: List Devices



```
GET https://connect.mindcloud.co/v1/universal/persona/latest/actions/list-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Persona `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/persona/latest/actions/list-devices?connectionId=$CONNECTION_ID&filterInquirySessionId=iqse_ABC123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filterInquirySessionId": "iqse_ABC123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/persona/latest/actions/list-devices?${params}`, {
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
| `filterInquirySessionId` | string | yes | Filter devices by inquiry session ID Example: `iqse_ABC123`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Persona API returns.

## Native endpoint

Through the native Persona API, this operation is `GET /devices` (base URL `https://api.withpersona.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-devices.md) for the provider-specific parameters and requirements.

