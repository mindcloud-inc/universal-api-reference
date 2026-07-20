# Placker: List Card Checklists



```
GET https://connect.mindcloud.co/v1/universal/placker/latest/actions/list-card-checklists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placker/latest/actions/list-card-checklists?connectionId=$CONNECTION_ID&card=1235" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "card": "1235"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placker/latest/actions/list-card-checklists?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `card` | number | yes | Card ID. Example: `1235`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "items": [
        {}
      ],
      "position": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Checklist ID. |
| `items` | array<object> | Checklist items. |
| `position` | number | Checklist position. |
| `title` | string | Checklist title. |

## Native endpoint

Through the native Placker API, this operation is `GET /card/:card/checklist` (base URL `https://api.placker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-card-checklists.md) for the provider-specific parameters and requirements.

