# Freshsales Classic: List Sales Activity Types

Retrieves sales activity types from Freshsales Classic.

```
GET https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-sales-activity-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshsales Classic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-sales-activity-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-sales-activity-types?${params}`, {
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
      "id": 1,
      "internalName": "Ava Chen",
      "isCheckedin": true,
      "isCheckedinMandatory": true,
      "isDefault": true,
      "isOutcomeMandatory": true,
      "name": "Ava Chen",
      "partial": true,
      "position": 1,
      "showInConversation": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Unique ID of the sales activity type. |
| `internalName` | string | Freshsales internal name for the activity type. |
| `isCheckedin` | boolean | Whether the activity type supports check-in. |
| `isCheckedinMandatory` | boolean | Whether check-in is mandatory for the activity type. |
| `isDefault` | boolean | Whether the activity type is a default type. |
| `isOutcomeMandatory` | boolean | Whether an outcome is mandatory for the activity type. |
| `name` | string | Sales activity type name. |
| `partial` | boolean | Whether the response row is a partial representation. |
| `position` | number | Display order of the activity type. |
| `showInConversation` | boolean | Whether the activity type appears in conversation views. |

## Native endpoint

Through the native Freshsales Classic API, this operation is `GET /selector/sales_activity_types` (base URL `https://{{credentials.bundleAlias}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sales-activity-types.md) for the provider-specific parameters and requirements.

