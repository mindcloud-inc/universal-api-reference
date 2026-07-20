# CATS: Get Company

Retrieves details for a company in CATS.

```
GET https://connect.mindcloud.co/v1/universal/cATS/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/get-company?connectionId=$CONNECTION_ID&id=23102956" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "23102956"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cATS/latest/actions/get-company?${params}`, {
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
| `id` | number | yes | The ID of the company to return. Example: `23102956`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "city": "string",
        "postalCode": "string",
        "state": "string",
        "street": "string"
      },
      "billingContactId": 1,
      "countryCode": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateModified": "2026-05-07T12:00:00.000Z",
      "enteredById": 1,
      "id": 1,
      "isHot": true,
      "keyTechnologies": "string",
      "name": "Ava Chen",
      "notes": "string",
      "ownerId": 1,
      "phones": {
        "fax": "string",
        "primary": "string",
        "secondary": "string"
      },
      "statusId": 1,
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.city` | string |  |
| `address.postalCode` | string |  |
| `address.state` | string |  |
| `address.street` | string |  |
| `billingContactId` | number |  |
| `countryCode` | string |  |
| `dateCreated` | date |  |
| `dateModified` | date |  |
| `enteredById` | number |  |
| `id` | number |  |
| `isHot` | boolean |  |
| `keyTechnologies` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `ownerId` | number |  |
| `phones.fax` | string |  |
| `phones.primary` | string |  |
| `phones.secondary` | string |  |
| `statusId` | number |  |
| `website` | string |  |

## Native endpoint

Through the native CATS API, this operation is `GET /companies/:id` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

