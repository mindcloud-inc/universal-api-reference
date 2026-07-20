# Remarkety: Batch Upsert Contacts



```
PUT https://connect.mindcloud.co/v1/universal/remarkety/latest/actions/batch-upsert-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Remarkety `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/remarkety/latest/actions/batch-upsert-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/remarkety/latest/actions/batch-upsert-contacts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contacts[]` | array<object> | yes |  |
| `update_existing` | boolean | no |  |
| `append_tags` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failed": 1,
      "failedReason": [
        {}
      ],
      "success": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failed` | number | Number of contacts that failed validation or processing. |
| `failedReason` | array<object> | Failure details for rejected contacts. |
| `success` | number | Number of contacts processed successfully. |

## Native endpoint

Through the native Remarkety API, this operation is `POST /api/v2/stores/{{credentials.storeId}}/contacts/batch` (base URL `https://app.remarkety.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-upsert-contacts.md) for the provider-specific parameters and requirements.

