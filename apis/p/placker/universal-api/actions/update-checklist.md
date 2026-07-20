# Placker: Update Checklist



```
PUT https://connect.mindcloud.co/v1/universal/placker/latest/actions/update-checklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/placker/latest/actions/update-checklist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checklist": "sjwa8k5le5p1c",
  "title": "Updated checklist title"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/placker/latest/actions/update-checklist', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "checklist": "sjwa8k5le5p1c",
    "title": "Updated checklist title"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checklist` | string | yes | Checklist ID. Example: `sjwa8k5le5p1c`. |
| `title` | string | yes | New title of the checklist. Example: `Updated checklist title`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Operation status. |

## Native endpoint

Through the native Placker API, this operation is `PATCH /checklist/:checklist` (base URL `https://api.placker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-checklist.md) for the provider-specific parameters and requirements.

