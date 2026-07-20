# CustomerX: Delete Financial By External ID

Deletes an existing financial record from CustomerX by external ID.

```
DELETE https://connect.mindcloud.co/v1/universal/customerX/latest/actions/delete-financial-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomerX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/delete-financial-by-external-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerX/latest/actions/delete-financial-by-external-id?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "amount_paid": "string",
      "client": {},
      "client_id": 1,
      "created_at": "string",
      "date_due": "string",
      "date_issue": "string",
      "date_original_due": "string",
      "date_payment": "string",
      "description": "string",
      "discount_value": "string",
      "external_id_financial": "string",
      "id": 1,
      "identifier": "string",
      "status": "string",
      "updated_at": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount_paid` | string |  |
| `client` | object |  |
| `client_id` | number |  |
| `created_at` | string |  |
| `date_due` | string |  |
| `date_issue` | string |  |
| `date_original_due` | string |  |
| `date_payment` | string |  |
| `description` | string |  |
| `discount_value` | string |  |
| `external_id_financial` | string |  |
| `id` | number |  |
| `identifier` | string |  |
| `status` | string |  |
| `updated_at` | string |  |
| `value` | string |  |

## Native endpoint

Through the native CustomerX API, this operation is `DELETE /api/v1/financials` (base URL `https://sandbox.api.customerx.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-financial-by-external-id.md) for the provider-specific parameters and requirements.

