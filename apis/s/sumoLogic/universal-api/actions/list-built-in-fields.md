# Sumo Logic: List Built-In Fields

Retrieves built-in fields from your Sumo Logic account.

```
GET https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-built-in-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumo Logic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-built-in-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-built-in-fields?${params}`, {
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
      "fieldId": "string",
      "fieldName": "Ava Chen",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataType` | string |  |
| `fieldId` | string |  |
| `fieldName` | string |  |
| `state` | string |  |

## Native endpoint

Through the native Sumo Logic API, this operation is `GET /v1/fields/builtin` (base URL `https://api.sumologic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-built-in-fields.md) for the provider-specific parameters and requirements.

