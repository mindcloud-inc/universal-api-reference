# Gridfox: List Tables

Retrieves tables in a Gridfox project.

```
GET https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/list-tables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridfox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/list-tables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/list-tables?${params}`, {
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
        {}
      ],
      "name": "Ava Chen",
      "referenceFieldName": "Ava Chen",
      "singularName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | array<object> | Field definitions configured on the table. |
| `name` | string | Table name. |
| `referenceFieldName` | string | Reference field used for record lookup. |
| `singularName` | string | Singular table label. |

## Native endpoint

Through the native Gridfox API, this operation is `GET /tables` (base URL `https://api.gridfox.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tables.md) for the provider-specific parameters and requirements.

