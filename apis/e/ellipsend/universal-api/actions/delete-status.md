# Ellipsend: Delete Status

Deletes an existing status from Ellipsend.

```
DELETE https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/delete-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ellipsend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/delete-status?connectionId=$CONNECTION_ID&statusId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "statusId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/delete-status?${params}`, {
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
| `statusId` | number | yes | The status ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Ellipsend API, this operation is `DELETE /status/[:status_id]` (base URL `https://api.ellipsend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-status.md) for the provider-specific parameters and requirements.

