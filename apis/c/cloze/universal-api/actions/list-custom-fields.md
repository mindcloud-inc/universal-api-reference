# Cloze: List Custom Fields

Retrieves custom fields from Cloze.

```
GET https://connect.mindcloud.co/v1/universal/cloze/latest/actions/list-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/list-custom-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloze/latest/actions/list-custom-fields?${params}`, {
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
| `relationtype` | list<string> | no | Filter custom fields by relation type: person, project, or company. One of: `company`, `person`, `project`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorcode": 1,
      "list": [
        [
          {}
        ]
      ],
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorcode` | number | Error code. 0 means success |
| `list[]` | array<object> | Array of custom field definitions |
| `list[].description` | string | Custom field description |
| `list[].id` | string | Custom field id |
| `list[].name` | string | Custom field display name |
| `list[].type` | string | Custom field data type |
| `message` | string | If an error occurs, this is the human readable description |

## Native endpoint

Through the native Cloze API, this operation is `GET /v1/user/fields` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-fields.md) for the provider-specific parameters and requirements.

