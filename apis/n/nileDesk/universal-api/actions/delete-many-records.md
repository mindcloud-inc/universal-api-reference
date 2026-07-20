# NileDesk: Delete Many Records

Deletes multiple matched records from NileDesk.

```
DELETE https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/delete-many-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NileDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/delete-many-records?connectionId=$CONNECTION_ID&filters=%5Bobject%20Object%5D&template_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filters": "[object Object]",
  "template_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/delete-many-records?${params}`, {
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
| `filters` | object | yes | The NileDesk filter object used to select the records to delete. |
| `template_id` | string | yes | The NileDesk template containing the records to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `message` | string | Provider message describing the result. |
| `success` | boolean | Whether NileDesk accepted the request. |

## Native endpoint

Through the native NileDesk API, this operation is `POST /DeleteManyRecords` (base URL `https://app.niledesk.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-many-records.md) for the provider-specific parameters and requirements.

