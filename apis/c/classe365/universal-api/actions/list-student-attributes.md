# Classe365: List Student Attributes

Retrieves a list of student attributes from Classe365.

```
GET https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-student-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Classe365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-student-attributes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-student-attributes?${params}`, {
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
      "attributeId": "string",
      "attributeName": "Ava Chen",
      "attributeType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributeId` | string |  |
| `attributeName` | string |  |
| `attributeType` | string |  |

## Native endpoint

Through the native Classe365 API, this operation is `GET /rest/studentAttributes` (base URL `https://{{credentials.username}}.classe365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-student-attributes.md) for the provider-specific parameters and requirements.

