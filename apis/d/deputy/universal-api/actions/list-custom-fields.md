# Deputy: List Custom Fields

Retrieves the custom field list from Deputy.

```
GET https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-custom-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-custom-fields?${params}`, {
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
      "action": 1,
      "apiName": "Ava Chen",
      "conditionalRules": true,
      "created": "2026-05-07T12:00:00.000Z",
      "creator": 1,
      "deputyField": "string",
      "displayTiming": 1,
      "helptext": "string",
      "id": 1,
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "published": true,
      "sortOrder": "string",
      "system": "string",
      "triggerScript": 1,
      "type": 1,
      "validation": "string",
      "valuelist": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | number |  |
| `apiName` | string |  |
| `conditionalRules` | boolean |  |
| `created` | date |  |
| `creator` | number |  |
| `deputyField` | string |  |
| `displayTiming` | number |  |
| `helptext` | string |  |
| `id` | number |  |
| `modified` | date |  |
| `name` | string |  |
| `published` | boolean |  |
| `sortOrder` | string |  |
| `system` | string |  |
| `triggerScript` | number |  |
| `type` | number |  |
| `validation` | string |  |
| `valuelist` | array<string> |  |

## Native endpoint

Through the native Deputy API, this operation is `GET /api/v1/resource/CustomField` (base URL `https://{{credentials.endpoint}}.deputy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-fields.md) for the provider-specific parameters and requirements.

