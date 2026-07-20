# SureContact: Add Contacts to Tag

Adds contacts to an existing SureContact tag.

```
PUT https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/add-contacts-to-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureContact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/add-contacts-to-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactUuids[]": [
    "string"
  ],
  "tagUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/add-contacts-to-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactUuids[]": ["string"],
    "tagUuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactUuids[]` | array<string> | yes |  |
| `tagUuid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "name": "Ava Chen",
      "slug": "string",
      "usage_count": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `created_at` | date |  |
| `description` | string |  |
| `name` | string |  |
| `slug` | string |  |
| `usage_count` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native SureContact API, this operation is `POST api/v1/public/tags/:tag_uuid/contacts/add` (base URL `https://api.surecontact.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contacts-to-tag.md) for the provider-specific parameters and requirements.

