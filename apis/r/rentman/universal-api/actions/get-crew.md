# Rentman: Get Crew



```
GET https://connect.mindcloud.co/v1/universal/rentman/latest/actions/get-crew
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rentman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/get-crew?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rentman/latest/actions/get-crew?${params}`, {
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
| `id` | number | yes | Numeric Rentman crew identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "avatar": "string",
      "bank": "string",
      "city": "string",
      "coc_code": "string",
      "company_name": "Ava Chen",
      "contract": 1,
      "contract_date": "2026-05-07T12:00:00.000Z",
      "country": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "custom": {},
      "default_warehouse": "string",
      "displayname": "Ava Chen",
      "email": "ava@example.com",
      "external_reference": "string",
      "firstname": "Ava",
      "folder": "string",
      "housenumber": "string",
      "id": 1,
      "lastname": "Chen",
      "middle_name": "Ava Chen",
      "modified": "2026-05-07T12:00:00.000Z",
      "phone": "string",
      "postal_code": "string",
      "street": "string",
      "tags": "string",
      "updateHash": "string",
      "vat_code": "string",
      "vt_fullname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `avatar` | string |  |
| `bank` | string |  |
| `city` | string |  |
| `coc_code` | string |  |
| `company_name` | string |  |
| `contract` | number |  |
| `contract_date` | date |  |
| `country` | string |  |
| `created` | date |  |
| `custom` | object |  |
| `default_warehouse` | string |  |
| `displayname` | string |  |
| `email` | string |  |
| `external_reference` | string |  |
| `firstname` | string |  |
| `folder` | string |  |
| `housenumber` | string |  |
| `id` | number |  |
| `lastname` | string |  |
| `middle_name` | string |  |
| `modified` | date |  |
| `phone` | string |  |
| `postal_code` | string |  |
| `street` | string |  |
| `tags` | string |  |
| `updateHash` | string |  |
| `vat_code` | string |  |
| `vt_fullname` | string |  |

## Native endpoint

Through the native Rentman API, this operation is `GET /crew/:id` (base URL `https://api.rentman.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-crew.md) for the provider-specific parameters and requirements.

