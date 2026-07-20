# Simplicate: Update Invoice



```
PUT https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/update-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/update-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/update-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `comments` | string | no | Invoice comments. |
| `date` | string | no | Invoice date in YYYY-MM-DD format. |
| `id` | string | yes | Invoice identifier. |
| `myOrganizationProfileId` | string | no | My organization profile identifier. |
| `organizationId` | string | no | Invoice recipient organization identifier. |
| `projectId` | string | no | Related project identifier. |
| `reference` | string | no | Invoice reference. |
| `subject` | string | no | Invoice subject. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Simplicate API, this operation is `PUT /invoices/invoice/:id` (base URL `https://{{credentials.subdomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice.md) for the provider-specific parameters and requirements.

