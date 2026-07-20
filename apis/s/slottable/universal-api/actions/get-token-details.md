# Slottable: Get Token Details

Retrieves API token details from Slottable.

```
GET https://connect.mindcloud.co/v1/universal/slottable/latest/actions/get-token-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slottable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slottable/latest/actions/get-token-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slottable/latest/actions/get-token-details?${params}`, {
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
      "attributes": {
        "company_id": 1,
        "created_at": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "name": "Ava Chen"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.company_id` | number | Company id associated with this token. |
| `attributes.created_at` | date | Token creation timestamp. |
| `attributes.id` | number | Internal token numeric id. |
| `attributes.name` | string | Token display name. |
| `id` | string | Access token resource id. |
| `type` | string | JSON:API resource type. |

## Native endpoint

Through the native Slottable API, this operation is `GET /token` (base URL `https://slottable.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-details.md) for the provider-specific parameters and requirements.

