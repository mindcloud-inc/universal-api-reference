# Socket: Delete Alert Triage

Deletes an existing alert triage rule from Socket.

```
DELETE https://connect.mindcloud.co/v1/universal/socket/latest/actions/delete-alert-triage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/socket/latest/actions/delete-alert-triage?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/delete-alert-triage?${params}`, {
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
| `uuid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |

## Native endpoint

Through the native Socket API, this operation is `DELETE /orgs/:org_slug/triage/alerts/:uuid` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-alert-triage.md) for the provider-specific parameters and requirements.

