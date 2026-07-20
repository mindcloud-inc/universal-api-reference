# Zoho People: Delete Leave Request

Deletes a leave request from Zoho People.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/delete-leave-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/delete-leave-request?connectionId=$CONNECTION_ID&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/delete-leave-request?${params}`, {
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
| `recordId` | string | yes | Leave request record ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": 1
      },
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.id` | number |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho People API, this operation is `DELETE /api/v3/leave-tracker/leaves/:recordId` (base URL `https://people.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-leave-request.md) for the provider-specific parameters and requirements.

