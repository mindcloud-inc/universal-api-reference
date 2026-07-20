# Pipeline CRM: Delete Company

Deletes an existing company from Pipeline CRM.

```
DELETE https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/delete-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeline CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/delete-company?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/delete-company?${params}`, {
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
| `id` | number | yes | Company ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Pipeline CRM API, this operation is `DELETE /companies/:id` (base URL `https://api.pipelinecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-company.md) for the provider-specific parameters and requirements.

