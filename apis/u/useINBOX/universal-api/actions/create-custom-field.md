# UseINBOX: Create Custom Field

Creates a custom field in UseINBOX.

```
POST https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/create-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UseINBOX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/create-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Name": "Ava Chen",
  "Type": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/create-custom-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Name": "Ava Chen",
    "Type": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Name` | string | yes | Custom field name. |
| `Type` | number | yes | INBOX custom field type value. |

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

Through the native UseINBOX API, this operation is `POST /inbox/v1/customfields` (base URL `https://useapi.useinbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-field.md) for the provider-specific parameters and requirements.

