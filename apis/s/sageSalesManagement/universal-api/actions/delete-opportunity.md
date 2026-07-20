# Sage Sales Management: Delete Opportunity

Deletes an opportunity from Sage Sales Management.

```
DELETE https://connect.mindcloud.co/v1/universal/sageSalesManagement/latest/actions/delete-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sage Sales Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sageSalesManagement/latest/actions/delete-opportunity?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sageSalesManagement/latest/actions/delete-opportunity?${params}`, {
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
| `id` | string | yes | Opportunity ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Message` | string | Deletion result message |

## Native endpoint

Through the native Sage Sales Management API, this operation is `DELETE /opportunities/{{id}}` (base URL `https://api.forcemanager.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-opportunity.md) for the provider-specific parameters and requirements.

