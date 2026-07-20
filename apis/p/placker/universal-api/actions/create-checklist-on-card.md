# Placker: Create Checklist On Card



```
POST https://connect.mindcloud.co/v1/universal/placker/latest/actions/create-checklist-on-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/placker/latest/actions/create-checklist-on-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "card": "1235",
  "title": "New checklist"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/placker/latest/actions/create-checklist-on-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "card": "1235",
    "title": "New checklist"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `card` | number | yes | Card ID. Example: `1235`. |
| `title` | string | yes | Title of the checklist. Example: `New checklist`. |
| `position` | number | no | Position of the checklist. Example: `1000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The ID of the created checklist. |
| `status` | string | Operation status. |

## Native endpoint

Through the native Placker API, this operation is `POST /card/:card/checklist` (base URL `https://api.placker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-checklist-on-card.md) for the provider-specific parameters and requirements.

