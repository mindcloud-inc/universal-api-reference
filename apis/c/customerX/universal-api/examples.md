# CustomerX Universal API Examples

These examples use the MindCloud API key and CustomerX connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers

Retrieves a list of customers from CustomerX.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-customers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "cancellation_date": "string",
      "cep": "string",
      "city": "string",
      "client_group_id": "string",
      "client_segment_id": 1,
      "client_service_id": 1,
      "cnpj_cpf": "string",
      "company_name": "Ava Chen",
      "complement": "string",
      "contract_status": "string",
      "country": "string",
      "created_at": "string",
      "custom_attributes": [
        {}
      ],
      "date_register": "string",
      "district": "string",
      "document_type": "string",
      "email": "ava@example.com",
      "external_id_client": "string",
      "facebook": "string",
      "group": "string",
      "id": 1,
      "ie_rg": "string",
      "instagram": "string",
      "journey_products": [
        {}
      ],
      "linkedin": "https://example.com",
      "number": "string",
      "only_journey_by_contract": true,
      "parent_client": {},
      "phones": [
        {}
      ],
      "portfolio": {},
      "segment": {},
      "service": {},
      "site": "string",
      "state": "string",
      "street": "string",
      "tags": [
        {}
      ],
      "trading_name": "Ava Chen",
      "twitter": "string",
      "updated_at": "string",
      "youtube": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/customerX/latest/actions/list-customers).

## Add Customer Journey

Creates a customer journey link in CustomerX.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/add-customer-journey" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customerX/latest/actions/add-customer-journey', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "default_journey_id": 1,
      "description": "string",
      "first_step_as_in_progress": true,
      "id": 1,
      "is_customized": true,
      "start_next_step_on_complete_step": true,
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Customer Journey action reference](actions/add-customer-journey.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/customerX/latest/actions/add-customer-journey).
