# Corsizio Universal API Examples

These examples use the MindCloud API key and Corsizio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Details

Retrieves account details from a Corsizio account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/corsizio/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/corsizio/latest/actions/get-account-details?${params}`, {
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
      "ageGroups": [
        {
          "id": "string",
          "label": "string"
        }
      ],
      "alias": "string",
      "categories": [
        {
          "id": "string",
          "label": "string"
        }
      ],
      "contact": {
        "email": "ava@example.com",
        "name": "Ava Chen",
        "phone": "string"
      },
      "created": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "genders": [
        {
          "id": "string",
          "label": "string"
        }
      ],
      "id": "string",
      "levels": [
        {
          "id": "string",
          "label": "string"
        }
      ],
      "locations": [
        {
          "city": "string",
          "country": "string",
          "id": "string",
          "label": "string",
          "name": "Ava Chen",
          "state": "string",
          "street": "string",
          "zip": "string"
        }
      ],
      "name": "Ava Chen",
      "priceRanges": [
        {
          "from": 1,
          "id": "string",
          "label": "string",
          "to": 1,
          "value": "string"
        }
      ],
      "siteUrl": "https://example.com",
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Details action reference](actions/get-account-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/corsizio/latest/actions/get-account-details).
