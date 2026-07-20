# Momence: List Memberships



```
GET https://connect.mindcloud.co/v1/universal/momence/latest/actions/list-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Momence `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/momence/latest/actions/list-memberships?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/momence/latest/actions/list-memberships?${params}`, {
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Legacy membership identifier field. The tenant response was empty during validation, so only the minimum identifier attribute is backfilled for validator metadata. |

## Native endpoint

Through the native Momence API, this operation is `GET /Memberships` (base URL `https://momence.com/_api/primary/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-memberships.md) for the provider-specific parameters and requirements.

