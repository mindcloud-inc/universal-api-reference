# Cinode: Get Tag Type

Retrieves a tag type from Cinode.

```
GET https://connect.mindcloud.co/v1/universal/cinode/latest/actions/get-tag-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cinode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cinode/latest/actions/get-tag-type?connectionId=$CONNECTION_ID&companyId=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cinode/latest/actions/get-tag-type?${params}`, {
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
| `companyId` | number | yes | Cinode company identifier. |
| `id` | number | yes | Identifier of the tag type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Cinode API, this operation is `GET /v0.2/companies/:companyId/tag-types/:id` (base URL `https://api.cinode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tag-type.md) for the provider-specific parameters and requirements.

