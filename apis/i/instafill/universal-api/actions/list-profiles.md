# Instafill: List Profiles



```
GET https://connect.mindcloud.co/v1/universal/instafill/latest/actions/list-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instafill `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instafill/latest/actions/list-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instafill/latest/actions/list-profiles?${params}`, {
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
| `status` | string | no |  |
| `status` | string | no | Filter profiles by status. |
| `name` | string | no |  |
| `name` | string | no | Filter profiles by name. |
| `page` | number | no |  |
| `page` | number | no | Page number to fetch. |
| `size` | number | no |  |
| `size` | number | no | Number of profiles per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "profiles": [
        {}
      ],
      "total": 1,
      "totalAll": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `profiles` | array<object> | Profiles returned for the current page. |
| `total` | number | Total number of profiles in the current filtered result set. |
| `totalAll` | number | Total number of profiles across the workspace. |

## Native endpoint

Through the native Instafill API, this operation is `GET /v1/profiles` (base URL `https://api.instafill.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-profiles.md) for the provider-specific parameters and requirements.

