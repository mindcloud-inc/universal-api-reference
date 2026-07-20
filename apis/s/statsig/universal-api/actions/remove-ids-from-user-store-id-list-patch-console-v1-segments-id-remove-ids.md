# Statsig: Remove IDs from User Store ID List

Removes IDs from a user store ID list in Statsig.

```
DELETE https://connect.mindcloud.co/v1/universal/statsig/latest/actions/remove-ids-from-user-store-id-list-patch-console-v1-segments-id-remove-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/remove-ids-from-user-store-id-list-patch-console-v1-segments-id-remove-ids?connectionId=$CONNECTION_ID&id=string&ids=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "ids": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/remove-ids-from-user-store-id-list-patch-console-v1-segments-id-remove-ids?${params}`, {
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
| `id` | string | yes | id |
| `ids` | list | yes | Request body field. |
| `version` | number | no | Request body field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `PATCH /console/v1/segments/{id}/remove_ids` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-ids-from-user-store-id-list-patch-console-v1-segments-id-remove-ids.md) for the provider-specific parameters and requirements.

