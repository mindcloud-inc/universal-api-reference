# CNPJá: Get Office by Tax ID

Retrieves office details by tax ID from CNPJá.

```
GET https://connect.mindcloud.co/v1/universal/cNPJ/latest/actions/get-office-by-tax-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CNPJá `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taxId` | string | yes | CNPJ number without punctuation. Example: `37335118000180`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.city` | string |  |
| `address.country.id` | number |  |
| `address.country.name` | string |  |
| `address.details` | string |  |
| `address.district` | string |  |
| `address.municipality` | number |  |
| `address.number` | string |  |
| `address.state` | string |  |
| `address.street` | string |  |
| `address.zip` | string |  |
| `alias` | string |  |
| `company.equity` | number |  |
| `company.id` | number |  |
| `company.members[].person.age` | string |  |
| `company.members[].person.id` | string |  |
| `company.members[].person.name` | string |  |
| `company.members[].person.taxId` | string |  |
| `company.members[].person.type` | string |  |
| `company.members[].role.id` | number |  |
| `company.members[].role.text` | string |  |
| `company.members[].since` | string |  |
| `company.name` | string |  |
| `company.nature.id` | number |  |
| `company.nature.text` | string |  |
| `company.size.acronym` | string |  |
| `company.size.id` | number |  |
| `company.size.text` | string |  |
| `emails[].address` | string |  |
| `emails[].domain` | string |  |
| `emails[].ownership` | string |  |
| `founded` | string |  |
| `head` | boolean |  |
| `mainActivity.id` | number |  |
| `mainActivity.text` | string |  |
| `phones[].area` | string |  |
| `phones[].number` | string |  |
| `phones[].type` | string |  |
| `sideActivities[].id` | number |  |
| `sideActivities[].text` | string |  |
| `status.id` | number |  |
| `status.text` | string |  |
| `statusDate` | string |  |
| `taxId` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native CNPJá API, this operation is `GET /office/:taxId` (base URL `https://api.cnpja.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-office-by-tax-id.md) for the provider-specific parameters and requirements.

