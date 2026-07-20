# Tidio: List Departments [Plus plan]

Retrieves departments from the Tidio workspace.

```
GET https://connect.mindcloud.co/v1/universal/tidio/latest/actions/list-departments-plus-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/list-departments-plus-plan?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tidio/latest/actions/list-departments-plus-plan?${params}`, {
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
      "departments": [
        {
          "id": "string",
          "name": "Ava Chen"
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
| `departments` | array<object> |  |
| `departments[]` | object |  |
| `departments[].id` | string | ID of the department |
| `departments[].name` | string | Name of the department |

## Native endpoint

Through the native Tidio API, this operation is `GET /departments` (base URL `https://api.tidio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-departments-plus-plan.md) for the provider-specific parameters and requirements.

