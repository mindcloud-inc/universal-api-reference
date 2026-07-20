# Cutt.ly: Set ABC Test

Sets an ABC test for a shortened link in Cutt.ly.

```
PUT https://connect.mindcloud.co/v1/universal/cuttly/latest/actions/set-abc-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cutt.ly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cuttly/latest/actions/set-abc-test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "edit": "string",
  "abtest_b": 1,
  "abtest_bvariation": "string",
  "abtest_c": 1,
  "abtest_cvariation": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cuttly/latest/actions/set-abc-test', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "edit": "string",
    "abtest_b": 1,
    "abtest_bvariation": "string",
    "abtest_c": 1,
    "abtest_cvariation": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `edit` | string | yes | The short link to edit. |
| `abtest_b` | number | yes | Traffic percentage to send to variation B. |
| `abtest_bvariation` | string | yes | Destination URL for variation B. |
| `abtest_c` | number | yes | Traffic percentage to send to variation C. |
| `abtest_cvariation` | string | yes | Destination URL for variation C. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number | Provider status code for the operation. |

## Native endpoint

Through the native Cutt.ly API, this operation is `GET /api.php` (base URL `https://cutt.ly/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-abc-test.md) for the provider-specific parameters and requirements.

