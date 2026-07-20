# Freshworks CRM: List Sales Activity Fields

Retrieves sales activity fields from Freshworks CRM.

```
GET https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-sales-activity-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-sales-activity-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-sales-activity-fields?${params}`, {
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
      "fields": [
        {
          "actionable": true,
          "base_model": "string",
          "choices": [
            {
              "id": "string",
              "position": 1,
              "value": "string"
            }
          ],
          "default": true,
          "id": 1,
          "label": "string",
          "name": "Ava Chen",
          "position": 1,
          "quick_add_position": 1,
          "required": true,
          "type": "string",
          "visible": true
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
| `fields[].actionable` | boolean |  |
| `fields[].base_model` | string |  |
| `fields[].choices[].id` | string |  |
| `fields[].choices[].position` | number |  |
| `fields[].choices[].value` | string |  |
| `fields[].default` | boolean |  |
| `fields[].id` | number |  |
| `fields[].label` | string |  |
| `fields[].name` | string |  |
| `fields[].position` | number |  |
| `fields[].quick_add_position` | number |  |
| `fields[].required` | boolean |  |
| `fields[].type` | string |  |
| `fields[].visible` | boolean |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `GET /api/settings/sales_activities/fields` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sales-activity-fields.md) for the provider-specific parameters and requirements.

