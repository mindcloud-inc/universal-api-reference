# Tiledesk: Delete Department

Deletes a department from the current Tiledesk project.

```
DELETE https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/delete-department
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiledesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/delete-department?connectionId=$CONNECTION_ID&depId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "depId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/delete-department?${params}`, {
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
| `depId` | string | yes | The department identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
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
| `_id` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Tiledesk API, this operation is `DELETE /{{credentials.projectId}}/departments/:depId` (base URL `https://api.tiledesk.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-department.md) for the provider-specific parameters and requirements.

