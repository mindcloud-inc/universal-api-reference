# CNPJá Universal API Examples

These examples use the MindCloud API key and CNPJá connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Office by Tax ID

Retrieves office details by tax ID from CNPJá.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cNPJ/latest/actions/get-office-by-tax-id?connectionId=$CONNECTION_ID&taxId=37335118000180" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taxId": "37335118000180"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cNPJ/latest/actions/get-office-by-tax-id?${params}`, {
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
      "address": {
        "city": "string",
        "country": {
          "id": 1,
          "name": "Ava Chen"
        },
        "details": "string",
        "district": "string",
        "municipality": 1,
        "number": "string",
        "state": "string",
        "street": "string",
        "zip": "string"
      },
      "alias": "string",
      "company": {
        "equity": 1,
        "id": 1,
        "members": [
          {
            "person": {
              "age": "string",
              "id": "string",
              "name": "Ava Chen",
              "taxId": "string",
              "type": "string"
            },
            "role": {
              "id": 1,
              "text": "string"
            },
            "since": "string"
          }
        ],
        "name": "Ava Chen",
        "nature": {
          "id": 1,
          "text": "string"
        },
        "size": {
          "acronym": "string",
          "id": 1,
          "text": "string"
        }
      },
      "emails": [
        {
          "address": "ava@example.com",
          "domain": "ava@example.com",
          "ownership": "ava@example.com"
        }
      ],
      "founded": "string",
      "head": true,
      "mainActivity": {
        "id": 1,
        "text": "string"
      },
      "phones": [
        {
          "area": "string",
          "number": "string",
          "type": "string"
        }
      ],
      "sideActivities": [
        {
          "id": 1,
          "text": "string"
        }
      ],
      "status": {
        "id": 1,
        "text": "string"
      },
      "statusDate": "string",
      "taxId": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Office by Tax ID action reference](actions/get-office-by-tax-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cNPJ/latest/actions/get-office-by-tax-id).
