# Buy Me a Coffee Universal API Examples

These examples use the MindCloud API key and Buy Me a Coffee connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Onetime Supporters

Retrieves onetime supporters from Buy Me a Coffee.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/list-onetime-supporters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/list-onetime-supporters?${params}`, {
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
      "currentPage": 1,
      "data": [
        {
          "country": "string",
          "isRefunded": true,
          "payerEmail": "ava@example.com",
          "payerName": "Ava Chen",
          "paymentPlatform": "string",
          "referer": "string",
          "supportCoffeePrice": "string",
          "supportCoffees": 1,
          "supportCreatedOn": "2026-05-07T12:00:00.000Z",
          "supportCurrency": "string",
          "supportEmail": "ava@example.com",
          "supporterName": "Ava Chen",
          "supportId": 1,
          "supportNote": "string",
          "supportNotePinned": 1,
          "supportUpdatedOn": "2026-05-07T12:00:00.000Z",
          "supportVisibility": 1,
          "transactionId": "string",
          "transferId": "string"
        }
      ],
      "firstPageUrl": "https://example.com",
      "from": 1,
      "lastPage": 1,
      "lastPageUrl": "https://example.com",
      "nextPageUrl": "https://example.com",
      "path": "string",
      "perPage": 1,
      "prevPageUrl": "https://example.com",
      "to": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [List Onetime Supporters action reference](actions/list-onetime-supporters.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/buyMeACoffee/latest/actions/list-onetime-supporters).
