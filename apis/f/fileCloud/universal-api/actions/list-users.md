# FileCloud: List Users

Retrieves users from FileCloud.

```
GET https://connect.mindcloud.co/v1/universal/fileCloud/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FileCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fileCloud/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fileCloud/latest/actions/list-users?${params}`, {
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
| `filter` | string | no | SCIM filter expression. |
| `sortBy` | string | no | Provider-specific sort field token. Verified values include username and emailid. |
| `sortOrder` | string | no | Sort direction. Verified values include ascending and descending. |
| `startIndex` | number | no | 1-based start index. |
| `count` | number | no | Maximum number of results to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "itemsPerPage": 1,
      "Resources": [
        {}
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
| `itemsPerPage` | number |  |
| `Resources` | array<object> |  |
| `schemas` | array<string> |  |
| `startIndex` | number |  |
| `totalResults` | number |  |

## Native endpoint

Through the native FileCloud API, this operation is `GET /scim/Users` (base URL `https://mindcloud.filecloudtrial.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

