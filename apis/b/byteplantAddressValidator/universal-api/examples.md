# Byteplant Address Validator Universal API Examples

These examples use the MindCloud API key and Byteplant Address Validator connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Address

Retrieves address validation results from Byteplant Address Validator.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/byteplantAddressValidator/latest/actions/verify-address?connectionId=$CONNECTION_ID&streetAddress=string&countryCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "streetAddress": "string",
  "countryCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/byteplantAddressValidator/latest/actions/verify-address?${params}`, {
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
      "addressline1": "string",
      "addresslinelast": "string",
      "city": "string",
      "corrections": "string",
      "cost": 1,
      "country": "string",
      "county": "string",
      "formattedaddress": "string",
      "latitude": 1,
      "longitude": 1,
      "postalcode": "string",
      "ratelimit_remain": 1,
      "ratelimit_seconds": 1,
      "rdi": "string",
      "state": "string",
      "status": "string",
      "street": "string",
      "streetnumber": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Verify Address action reference](actions/verify-address.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/byteplantAddressValidator/latest/actions/verify-address).

## Start Bulk Address Validation

Creates a bulk address validation task in Byteplant Address Validator.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/byteplantAddressValidator/latest/actions/start-bulk-address-validation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "addressesCsv": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/byteplantAddressValidator/latest/actions/start-bulk-address-validation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "addressesCsv": "string"
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
      "info": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Start Bulk Address Validation action reference](actions/start-bulk-address-validation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/byteplantAddressValidator/latest/actions/start-bulk-address-validation).
