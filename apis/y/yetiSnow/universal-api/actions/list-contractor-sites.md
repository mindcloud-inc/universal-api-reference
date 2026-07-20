# Yeti Snow: List Contractor Sites



```
GET https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/list-contractor-sites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yeti Snow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/list-contractor-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/list-contractor-sites?${params}`, {
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
| `contractorId` | string | no | Contractor identifier from List Contractors. |
| `page` | string | no | Page number to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "current_page": 1,
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_page` | number | Current page number. |
| `data` | array<object> | Sites linked to the contractor. |

## Native endpoint

Through the native Yeti Snow API, this operation is `GET contractor/show/{{contractor_id}}/sites` (base URL `https://sandbox_api.yetisoftware.com/api/en/public_access/1715`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contractor-sites.md) for the provider-specific parameters and requirements.

