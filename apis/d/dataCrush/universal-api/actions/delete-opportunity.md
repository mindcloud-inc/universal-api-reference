# DataCrush: Delete Opportunity

Deletes an existing opportunity from DataCrush.

```
DELETE https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/delete-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataCrush `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/delete-opportunity?connectionId=$CONNECTION_ID&opportunity_key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "opportunity_key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/delete-opportunity?${params}`, {
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
| `opportunity_key` | string | yes | Opportunity key to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |

## Native endpoint

Through the native DataCrush API, this operation is `POST /crm/opportunity/delete` (base URL `https://api.datacrush.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-opportunity.md) for the provider-specific parameters and requirements.

