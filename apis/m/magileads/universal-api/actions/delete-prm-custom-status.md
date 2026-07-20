# Magileads: Delete PRM Custom Status

Deletes a custom PRM status from Magileads.

```
DELETE https://connect.mindcloud.co/v1/universal/magileads/latest/actions/delete-prm-custom-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Magileads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/magileads/latest/actions/delete-prm-custom-status?connectionId=$CONNECTION_ID&status_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "status_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/magileads/latest/actions/delete-prm-custom-status?${params}`, {
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
| `status_id` | number | yes | The custom status ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "state": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `state` | boolean |  |

## Native endpoint

Through the native Magileads API, this operation is `DELETE /prm/status/custom/:status_id` (base URL `https://app.api-magileads.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-prm-custom-status.md) for the provider-specific parameters and requirements.

