# UseINBOX: Update Custom Field

Updates an existing custom field in UseINBOX.

```
PUT https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/update-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UseINBOX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/update-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/update-custom-field', {
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
| `id` | string | yes | Custom field ID from INBOX. |
| `Name` | string | no | Updated custom field name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "Name": "Ava Chen",
      "Type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `Name` | string |  |
| `Type` | number |  |

## Native endpoint

Through the native UseINBOX API, this operation is `PATCH /inbox/v1/customfields/:id` (base URL `https://useapi.useinbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-custom-field.md) for the provider-specific parameters and requirements.

