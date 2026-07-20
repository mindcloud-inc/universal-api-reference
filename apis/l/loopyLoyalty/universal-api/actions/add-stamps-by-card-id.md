# Loopy Loyalty: Add Stamps By Card ID



```
PUT https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/add-stamps-by-card-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/add-stamps-by-card-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cid": "RDX5AsgKYa3UZ7",
  "stamps": "10"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/add-stamps-by-card-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cid": "RDX5AsgKYa3UZ7",
    "stamps": "10"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cid` | string | yes | Card ID to add or deduct stamps on. Example: `RDX5AsgKYa3UZ7`. |
| `stamps` | number | yes | Number of stamps to add. Negative values deduct stamps. Example: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scanLatitude` | number | no | Optional latitude where the scan took place. Example: `42.3876`. |
| `scanLongitude` | number | no | Optional longitude where the scan took place. Example: `-71.2110`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the stamps were applied successfully. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `POST /card/cid/:cid/addStamps/:stamps` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-stamps-by-card-id.md) for the provider-specific parameters and requirements.

