# RevenueCat: Delete Offering

Deletes an offering and packages from RevenueCat.

```
DELETE https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/delete-offering
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RevenueCat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/delete-offering?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/delete-offering?${params}`, {
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
      "deleted_at": "string",
      "id": "string",
      "items": [
        {}
      ],
      "object": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted_at` | string |  |
| `id` | string |  |
| `items` | array<object> |  |
| `object` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native RevenueCat API, this operation is `DELETE projects/:projectId/offerings/:offeringId` (base URL `https://api.revenuecat.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-offering.md) for the provider-specific parameters and requirements.

