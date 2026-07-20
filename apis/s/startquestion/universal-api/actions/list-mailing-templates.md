# Startquestion: List Mailing Templates

Retrieves mailing templates from Startquestion.

```
GET https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/list-mailing-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Startquestion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/list-mailing-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/list-mailing-templates?${params}`, {
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
      "list": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `list` | array<object> | Mailing templates. |
| `total` | number | Total number of mailing templates. |

## Native endpoint

Through the native Startquestion API, this operation is `GET /mailing/templates` (base URL `https://www.startquestion.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mailing-templates.md) for the provider-specific parameters and requirements.

