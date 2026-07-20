# SAP ERP (S/4HANA) Universal API Examples

These examples use the MindCloud API key and SAP ERP (S/4HANA) connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Business Partners

Retrieves business partners from SAP ERP (S/4HANA).

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partners?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partners?${params}`, {
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
      "businessPartner": "string",
      "businessPartnerCategory": "string",
      "businessPartnerFullName": "Ava Chen",
      "businessPartnerGrouping": "string",
      "businessPartnerName": "Ava Chen",
      "businessPartnerUUID": "string",
      "createdByUser": "string",
      "creationDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Business Partners action reference](actions/list-business-partners.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sAPERPS4HANA/latest/actions/list-business-partners).
