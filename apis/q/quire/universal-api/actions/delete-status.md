# Quire: Delete Status

Deletes an existing status from Quire.

```
DELETE https://connect.mindcloud.co/v1/universal/quire/latest/actions/delete-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/quire/latest/actions/delete-status?connectionId=$CONNECTION_ID&projectId=string&value=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "value": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quire/latest/actions/delete-status?${params}`, {
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
| `projectId` | string | yes | The project ID or shortcut, for example App_Account. |
| `value` | number | yes | Numeric status value to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Quire API, this operation is `DELETE status/id/:projectId/:value` (base URL `https://quire.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-status.md) for the provider-specific parameters and requirements.

