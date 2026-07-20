# Ecologi: Get Total Number of Trees

Retrieves total trees planted from Ecologi.

```
GET https://connect.mindcloud.co/v1/universal/ecologi/latest/actions/get-total-number-of-trees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ecologi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ecologi/latest/actions/get-total-number-of-trees?connectionId=$CONNECTION_ID&username=business-name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "business-name"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ecologi/latest/actions/get-total-number-of-trees?${params}`, {
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
| `username` | string | yes | Your Ecologi username. Example: `business-name`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pending": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pending` | number | All unpaid trees for this user. |
| `total` | number | All paid trees for this user. |

## Native endpoint

Through the native Ecologi API, this operation is `GET /users/:username/trees` (base URL `https://public.ecologi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-total-number-of-trees.md) for the provider-specific parameters and requirements.

