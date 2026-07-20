# Companies House: Get Disqualified Natural Officer

Retrieves a disqualified natural officer from Companies House.

```
GET https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-disqualified-natural-officer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Companies House `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-disqualified-natural-officer?connectionId=$CONNECTION_ID&officerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "officerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-disqualified-natural-officer?${params}`, {
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
| `officerId` | string | yes | The disqualified natural officer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date_of_birth": "string",
      "disqualifications": [
        "string"
      ],
      "etag": "string",
      "forename": "Ava Chen",
      "honours": "string",
      "kind": "string",
      "links": {},
      "nationality": "string",
      "other_forenames": "Ava Chen",
      "permissions_to_act": [
        "string"
      ],
      "person_number": "string",
      "surname": "Ava Chen",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date_of_birth` | string |  |
| `disqualifications` | array |  |
| `etag` | string |  |
| `forename` | string |  |
| `honours` | string |  |
| `kind` | string |  |
| `links` | object |  |
| `nationality` | string |  |
| `other_forenames` | string |  |
| `permissions_to_act` | array |  |
| `person_number` | string |  |
| `surname` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Companies House API, this operation is `GET /disqualified-officers/natural/:officer_id` (base URL `https://api.company-information.service.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-disqualified-natural-officer.md) for the provider-specific parameters and requirements.

