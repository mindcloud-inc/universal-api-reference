# OkoCRM: Delete company

Deletes an existing company from OkoCRM.

```
DELETE https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/delete-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OkoCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/delete-company?connectionId=$CONNECTION_ID&company_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "company_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/delete-company?${params}`, {
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
| `company_id` | number | yes | The OkoCRM company ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | number |  |

## Native endpoint

Through the native OkoCRM API, this operation is `DELETE /companies/[:company_id]/` (base URL `https://api.okocrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-company.md) for the provider-specific parameters and requirements.

