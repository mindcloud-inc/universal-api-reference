# Copperx Universal API Examples

These examples use the MindCloud API key and Copperx connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Copperx.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-current-user?${params}`, {
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
      "accountType": "string",
      "address": {},
      "createdAt": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "flags": {},
      "id": "string",
      "lastName": "Chen",
      "organization": {},
      "phone": "string",
      "position": "string",
      "profilePicture": "string",
      "role": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/copperx/latest/actions/get-current-user).

## Activate Payment Link

Activates a payment link in Copperx.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/copperx/latest/actions/activate-payment-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "linkId": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/copperx/latest/actions/activate-payment-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "linkId": "https://example.com"
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
      "afterCompletion": "string",
      "allowedChains": [
        {}
      ],
      "allowPromotionCodes": true,
      "amount": "string",
      "billingAddressCollection": true,
      "createdAt": "string",
      "currencies": [
        "string"
      ],
      "currency": "string",
      "customFields": {},
      "description": "string",
      "emailCollection": true,
      "id": "string",
      "image": "string",
      "isActive": true,
      "nameCollection": true,
      "organizationId": "string",
      "phoneNumberCollection": true,
      "preferredCurrency": "string",
      "priceType": "string",
      "productId": "string",
      "shippingAddressCollection": true,
      "submitType": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Activate Payment Link action reference](actions/activate-payment-link.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/copperx/latest/actions/activate-payment-link).
