# Jitbit Helpdesk: List Custom Fields for Category



```
GET https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-custom-fields-for-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jitbit Helpdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-custom-fields-for-category?connectionId=$CONNECTION_ID&categoryId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "categoryId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-custom-fields-for-category?${params}`, {
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
| `categoryId` | number | yes | Jitbit category ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fieldId": 1,
      "id": 1,
      "name": "Ava Chen",
      "type": "string",
      "valueType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fieldId` | number | Category custom field ID when present. |
| `id` | number | Field identifier when present. |
| `name` | string | Field name. |
| `type` | string | Field type. |
| `valueType` | string | Value type. |

## Native endpoint

Through the native Jitbit Helpdesk API, this operation is `GET /CustomFieldsForCategory` (base URL `{{credentials.helpdeskBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-fields-for-category.md) for the provider-specific parameters and requirements.

