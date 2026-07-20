# Trint: List SCIM Users

Retrieves SCIM users from Trint.

```
GET https://connect.mindcloud.co/v1/universal/trint/latest/actions/list-scim-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trint/latest/actions/list-scim-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trint/latest/actions/list-scim-users?${params}`, {
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
      "itemsPerPage": 1,
      "Resources": [
        {
          "id": "string",
          "userName": "Ava Chen"
        }
      ],
      "schemas": [
        "string"
      ],
      "startIndex": 1,
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `itemsPerPage` | number | Number of SCIM resources returned in this page. |
| `Resources` | array<object> | Matched SCIM resources. |
| `Resources[].id` | string | SCIM resource identifier. |
| `Resources[].userName` | string | SCIM username when the resource is a user. |
| `schemas` | array<string> | SCIM schema identifiers for the response envelope. |
| `startIndex` | number | SCIM page start index. |
| `totalResults` | number | Total number of matched SCIM resources. |

## Native endpoint

Through the native Trint API, this operation is `GET https://scim.trint.com/v2/Users` (base URL `https://api.trint.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-scim-users.md) for the provider-specific parameters and requirements.

