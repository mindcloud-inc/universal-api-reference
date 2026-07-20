# Snappy Universal API Examples

These examples use the MindCloud API key and Snappy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Keys

Retrieves API keys from Snappy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snappy/latest/actions/get-api-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snappy/latest/actions/get-api-keys?${params}`, {
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
      "accountsAccess": {
        "ids": [
          "string"
        ],
        "scope": "string"
      },
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enforceMtls": true,
      "expirationDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "permissions": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get API Keys action reference](actions/get-api-keys.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/snappy/latest/actions/get-api-keys).

## Claim Gift

Claims an existing gift in Snappy.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/snappy/latest/actions/claim-gift" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "string",
  "giftId": "string",
  "orderRecipient": {},
  "variantId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/snappy/latest/actions/claim-gift', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "string",
    "giftId": "string",
    "orderRecipient": {},
    "variantId": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Claim Gift action reference](actions/claim-gift.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/snappy/latest/actions/claim-gift).
