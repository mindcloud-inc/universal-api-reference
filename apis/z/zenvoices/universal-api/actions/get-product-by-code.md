# Zenvoices: Get Product By Code

Retrieves a product from Zenvoices by code.

```
GET https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/get-product-by-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenvoices `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/get-product-by-code?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/get-product-by-code?${params}`, {
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
      "administrationId": 1,
      "code": "string",
      "externalId": "string",
      "isActive": true,
      "name": "Ava Chen",
      "productType": 1,
      "purchasePrice": 1,
      "salesPrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `administrationId` | number | administrationId returned by Zenvoices. |
| `code` | string | code returned by Zenvoices. |
| `externalId` | string | externalId returned by Zenvoices. |
| `isActive` | boolean | isActive returned by Zenvoices. |
| `name` | string | name returned by Zenvoices. |
| `productType` | number | productType returned by Zenvoices. |
| `purchasePrice` | number | purchasePrice returned by Zenvoices. |
| `salesPrice` | number | salesPrice returned by Zenvoices. |

## Native endpoint

Through the native Zenvoices API, this operation is `GET /public-api/v1/product` (base URL `https://app.zenvoices.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-by-code.md) for the provider-specific parameters and requirements.

