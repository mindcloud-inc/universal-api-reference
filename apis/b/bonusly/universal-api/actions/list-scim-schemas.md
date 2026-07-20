# Bonusly: List SCIM Schemas

Retrieves SCIM schemas from Bonusly.

```
GET https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/list-scim-schemas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bonusly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/list-scim-schemas?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/list-scim-schemas?${params}`, {
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
      "Resources": [
        {}
      ],
      "schemas": [
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
| `Resources` | array<object> |  |
| `schemas` | array<string> |  |

## Native endpoint

Through the native Bonusly API, this operation is `GET https://bonus.ly/api/scim11/Schemas` (base URL `https://bonus.ly/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-scim-schemas.md) for the provider-specific parameters and requirements.

