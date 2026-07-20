# Companies House: Get Disqualified Corporate Officer

Retrieves a disqualified corporate officer from Companies House.

```
GET https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-disqualified-corporate-officer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Companies House `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-disqualified-corporate-officer?connectionId=$CONNECTION_ID&officerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "officerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-disqualified-corporate-officer?${params}`, {
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
| `officerId` | string | yes | The disqualified corporate officer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_number": "string",
      "country_of_registration": "string",
      "disqualifications": [
        "string"
      ],
      "etag": "string",
      "kind": "string",
      "links": {},
      "name": "Ava Chen",
      "permissions_to_act": [
        "string"
      ],
      "person_number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_number` | string |  |
| `country_of_registration` | string |  |
| `disqualifications` | array |  |
| `etag` | string |  |
| `kind` | string |  |
| `links` | object |  |
| `name` | string |  |
| `permissions_to_act` | array |  |
| `person_number` | string |  |

## Native endpoint

Through the native Companies House API, this operation is `GET /disqualified-officers/corporate/:officer_id` (base URL `https://api.company-information.service.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-disqualified-corporate-officer.md) for the provider-specific parameters and requirements.

