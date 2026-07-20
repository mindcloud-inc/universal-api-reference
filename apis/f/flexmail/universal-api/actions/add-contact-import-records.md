# Flexmail: Add Contact Import Records

Adds records to a contact import in Flexmail.

```
PUT https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/add-contact-import-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexmail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/add-contact-import-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "records[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/add-contact-import-records', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "records[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `records[]` | array<object> | yes | JSON array of contact import records. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Placeholder schema for the documented no-content success response. |

## Native endpoint

Through the native Flexmail API, this operation is `POST /contacts/imports/{id}/records` (base URL `https://api.flexmail.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact-import-records.md) for the provider-specific parameters and requirements.

