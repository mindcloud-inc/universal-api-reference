# Tax ID Pro Universal API Examples

These examples use the MindCloud API key and Tax ID Pro connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Tax ID

Retrieves a tax ID validation from Tax ID Pro.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taxIDPro/latest/actions/validate-tax-id?connectionId=$CONNECTION_ID&country=string&tin=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "string",
  "tin": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taxIDPro/latest/actions/validate-tax-id?${params}`, {
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
      "country_name": "Ava Chen",
      "format_name": "Ava Chen",
      "is_valid": true,
      "message": "string",
      "tin_compact": "string",
      "tin_standard": "string"
    }
  ],
  "meta": {}
}
```

See the full [Validate Tax ID action reference](actions/validate-tax-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/taxIDPro/latest/actions/validate-tax-id).

## Batch Validate Tax IDs

Creates batch tax ID validations in Tax ID Pro.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/taxIDPro/latest/actions/batch-validate-tax-ids" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "validations[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/taxIDPro/latest/actions/batch-validate-tax-ids', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "validations[]": [{}]
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
      "country_name": "Ava Chen",
      "error_code": "string",
      "format_name": "Ava Chen",
      "is_valid": true,
      "message": "string",
      "reference_id": "string",
      "tin_compact": "string",
      "tin_standard": "string"
    }
  ],
  "meta": {}
}
```

See the full [Batch Validate Tax IDs action reference](actions/batch-validate-tax-ids.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/taxIDPro/latest/actions/batch-validate-tax-ids).
