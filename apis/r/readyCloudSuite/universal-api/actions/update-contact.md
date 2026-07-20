# ReadyCloud Suite: Update Contact

Updates an existing contact in ReadyCloud Suite.

```
PUT https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReadyCloud Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactPk": "string",
  "orgPk": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactPk": "string",
    "orgPk": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactPk` | string | yes | ReadyCloud contact identifier. |
| `orgPk` | string | yes | ReadyCloud organization identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_fields": {},
      "description": "string",
      "first_name": "Ava",
      "is_company": true,
      "last_name": "Chen",
      "notes": [
        {}
      ],
      "occupation": "string",
      "orders": "string",
      "profile_image": "string",
      "source": {},
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `created_at` | date |  |
| `custom_fields` | object |  |
| `description` | string |  |
| `first_name` | string |  |
| `is_company` | boolean |  |
| `last_name` | string |  |
| `notes` | array<object> |  |
| `occupation` | string |  |
| `orders` | string |  |
| `profile_image` | string |  |
| `source` | object |  |
| `updated_at` | date |  |
| `url` | string |  |
| `website` | string |  |

## Native endpoint

Through the native ReadyCloud Suite API, this operation is `PATCH /api/v2/orgs/:orgPk/contacts/:contactPk/` (base URL `https://www.readycloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

