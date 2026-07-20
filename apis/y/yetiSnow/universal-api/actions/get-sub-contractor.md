# Yeti Snow: Get Sub-contractor



```
GET https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/get-sub-contractor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yeti Snow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/get-sub-contractor?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/get-sub-contractor?${params}`, {
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
| `subContractorId` | string | no | Sub-contractor identifier from List Sub-contractors. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the sub-contractor is active. |
| `id` | string | Sub-contractor identifier. |
| `name` | string | Sub-contractor name. |

## Native endpoint

Through the native Yeti Snow API, this operation is `GET sub_contractor/show/{{sub_contractor_id}}` (base URL `https://sandbox_api.yetisoftware.com/api/en/public_access/1715`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sub-contractor.md) for the provider-specific parameters and requirements.

