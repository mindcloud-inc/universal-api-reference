# UseINBOX: Import Contacts To List

Imports contacts into a list in UseINBOX.

```
POST https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/import-contacts-to-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UseINBOX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/import-contacts-to-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactlistId": "string",
  "contacts[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/import-contacts-to-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactlistId": "string",
    "contacts[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactlistId` | string | yes | Contact list ID that will receive the imported contacts. |
| `contacts[]` | array<object> | yes | Array of contact objects to import. Each object should follow the documented INBOX import shape with email and optional customFields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "importedCount": 1,
      "status": "string",
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `importedCount` | number |  |
| `status` | string |  |
| `totalCount` | number |  |

## Native endpoint

Through the native UseINBOX API, this operation is `POST /inbox/v1/contactlists/:contactlistId/import` (base URL `https://useapi.useinbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-contacts-to-list.md) for the provider-specific parameters and requirements.

