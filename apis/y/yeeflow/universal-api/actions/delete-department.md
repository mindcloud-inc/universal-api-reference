# Yeeflow: Delete Department



```
DELETE https://connect.mindcloud.co/v1/universal/yeeflow/latest/actions/delete-department
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yeeflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/yeeflow/latest/actions/delete-department?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yeeflow/latest/actions/delete-department?${params}`, {
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
| `id` | string | no | Department ID from Yeeflow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Data": "string",
      "Message": "string",
      "Status": 1,
      "TotalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Data` | string |  |
| `Message` | string |  |
| `Status` | number |  |
| `TotalCount` | number |  |

## Native endpoint

Through the native Yeeflow API, this operation is `DELETE /departments/:id` (base URL `https://api.yeeflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-department.md) for the provider-specific parameters and requirements.

