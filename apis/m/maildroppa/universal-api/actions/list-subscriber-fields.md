# Maildroppa: List Subscriber Fields



```
GET https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/list-subscriber-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildroppa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/list-subscriber-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/list-subscriber-fields?${params}`, {
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
      "dataType": "string",
      "id": "string",
      "isDefault": true,
      "isMandatory": true,
      "name": "Ava Chen",
      "optionValues": [
        "string"
      ],
      "personalizationTagName": "Ava Chen",
      "used": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataType` | string | Specifies the data type for this field (e.g., TEXT, NUMBER, DATE). |
| `id` | string | Unique identifier of the field type. |
| `isDefault` | boolean | Indicates whether this field type is system-provided and cannot be removed. |
| `isMandatory` | boolean | Indicates whether this field type must always have a value. |
| `name` | string | Display name of the field type. |
| `optionValues` | array<string> | List of allowable values if the data type is a choice-based type. |
| `personalizationTagName` | string | Name of the personalization tag associated with this field. |
| `used` | boolean | Indicates if this field type is currently used by any subscribers. |

## Native endpoint

Through the native Maildroppa API, this operation is `GET /field-type` (base URL `https://api.maildroppa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscriber-fields.md) for the provider-specific parameters and requirements.

