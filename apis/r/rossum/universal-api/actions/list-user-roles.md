# Rossum: List User Roles

Retrieves user roles from Rossum.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-user-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-user-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-user-roles?${params}`, {
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
| `name` | string | no | Filter user roles by name. |
| `ordering` | string | no | Ordering expression, for example name or -name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "next": {},
        "previous": {}
      },
      "results": [
        {
          "id": 1,
          "name": "Ava Chen",
          "url": "https://example.com"
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
| `pagination.next` | object |  |
| `pagination.previous` | object |  |
| `results[].id` | number |  |
| `results[].name` | string |  |
| `results[].url` | string |  |

## Native endpoint

Through the native Rossum API, this operation is `GET /groups` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-roles.md) for the provider-specific parameters and requirements.

