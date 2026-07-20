# SmartReach: Add or Update Prospects

Finds prospects in SmartReach, or creates them if needed.

```
POST https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/add-or-update-prospects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/add-or-update-prospects" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prospects[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/add-or-update-prospects', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prospects[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uniqueIdentifierColumns` | string | no | Comma-separated list of columns to use as unique identifiers to find duplicates. Valid values: email, phone, linkedin_url, company_firstname_lastname. Defaults to "email" if not provided (backward compatible with existing behavior). Note: The order in which you specify columns does not matter. The system will always check for duplicates in this priority order: email, linkedin_url, phone, company_firstname_lastname. Examples: - "email" - Use only email to find duplicates (default) - "phone" - Use only phone to find duplicates - "linkedin_url" - Use only LinkedIn URL to find duplicates - "email,phone" - Use both email and phone to find duplicates - "email,phone,linkedin_url,company_firstname_lastname" - Use all four columns |
| `prospects[]` | array<object> | yes | Each prospect must have at least one unique identifier column: - email, OR - phone_number, OR - linkedin_url, OR - company + first_name + last_name (all three required together) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "created_at": "string",
      "emails": [
        {
          "email": "ava@example.com"
        }
      ],
      "first_name": "Ava",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `created_at` | string |  |
| `emails[].email` | string |  |
| `first_name` | string |  |
| `id` | string |  |

## Native endpoint

Through the native SmartReach API, this operation is `POST /prospects` (base URL `https://api.smartreach.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-or-update-prospects.md) for the provider-specific parameters and requirements.

