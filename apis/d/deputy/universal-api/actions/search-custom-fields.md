# Deputy: Search Custom Fields

Finds matching custom fields in Deputy.

```
GET https://connect.mindcloud.co/v1/universal/deputy/latest/actions/search-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deputy/latest/actions/search-custom-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deputy/latest/actions/search-custom-fields?${params}`, {
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
      "Action": 1,
      "ApiName": "Ava Chen",
      "ConditionalRules": true,
      "Created": "2026-05-07T12:00:00.000Z",
      "Creator": 1,
      "DeputyField": "string",
      "DisplayTiming": 1,
      "Helptext": "string",
      "Id": 1,
      "Modified": "2026-05-07T12:00:00.000Z",
      "Name": "Ava Chen",
      "Published": true,
      "SortOrder": "string",
      "System": "string",
      "TriggerScript": 1,
      "Type": 1,
      "Validation": "string",
      "Valuelist": [
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
| `Action` | number |  |
| `ApiName` | string |  |
| `ConditionalRules` | boolean |  |
| `Created` | date |  |
| `Creator` | number |  |
| `DeputyField` | string |  |
| `DisplayTiming` | number |  |
| `Helptext` | string |  |
| `Id` | number |  |
| `Modified` | date |  |
| `Name` | string |  |
| `Published` | boolean |  |
| `SortOrder` | string |  |
| `System` | string |  |
| `TriggerScript` | number |  |
| `Type` | number |  |
| `Validation` | string |  |
| `Valuelist` | array<string> |  |

## Native endpoint

Through the native Deputy API, this operation is `POST /api/v1/resource/CustomField/QUERY` (base URL `https://{{credentials.endpoint}}.deputy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-custom-fields.md) for the provider-specific parameters and requirements.

