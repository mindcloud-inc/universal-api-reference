# ECAL: Delete Private Event

Deletes a subscriber's private ECAL event.

```
DELETE https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/delete-private-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECAL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/delete-private-event?connectionId=$CONNECTION_ID&eventIdOrReference=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventIdOrReference": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/delete-private-event?${params}`, {
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
| `eventIdOrReference` | string | yes | Private event ID or reference accepted by the delete endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native ECAL API, this operation is `DELETE /event/:eventIdOrReference` (base URL `https://api.ecal.com/apiv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-private-event.md) for the provider-specific parameters and requirements.

