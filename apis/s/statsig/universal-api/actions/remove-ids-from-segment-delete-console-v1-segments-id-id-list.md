# Statsig: Remove IDs from Segment

Removes IDs from a segment in Statsig.

```
DELETE https://connect.mindcloud.co/v1/universal/statsig/latest/actions/remove-ids-from-segment-delete-console-v1-segments-id-id-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/remove-ids-from-segment-delete-console-v1-segments-id-id-list?connectionId=$CONNECTION_ID&id=string&ids=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "ids": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/remove-ids-from-segment-delete-console-v1-segments-id-id-list?${params}`, {
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

Through the native Statsig API, this operation is `DELETE /console/v1/segments/{id}/id_list` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-ids-from-segment-delete-console-v1-segments-id-id-list.md) for the provider-specific parameters and requirements.

