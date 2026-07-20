# Ziflow: List Decision Checklist

Retrieves decision checklist settings from Ziflow.

```
GET https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-decision-checklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ziflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-decision-checklist?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-decision-checklist?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "display_text": "string",
      "mandatory": true,
      "multiple_selection": true,
      "options": [
        {
          "id": "string",
          "label": "string",
          "order": 1,
          "text_field_available": true
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `display_text` | string |  |
| `mandatory` | boolean |  |
| `multiple_selection` | boolean |  |
| `options[].id` | string |  |
| `options[].label` | string |  |
| `options[].order` | number |  |
| `options[].text_field_available` | boolean |  |

## Native endpoint

Through the native Ziflow API, this operation is `GET /decision-checklist` (base URL `https://api.ziflow.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-decision-checklist.md) for the provider-specific parameters and requirements.

