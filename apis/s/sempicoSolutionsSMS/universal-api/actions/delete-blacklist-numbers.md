# Sempico Solutions SMS: Delete Blacklist Numbers



```
DELETE https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/delete-blacklist-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sempico Solutions SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/delete-blacklist-numbers?connectionId=$CONNECTION_ID&numbers%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "numbers[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/delete-blacklist-numbers?${params}`, {
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
| `numbers[]` | array<string> | yes | Phone numbers to delete from the personal blacklist. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blacklistDetails": {
        "countAfter": 1,
        "countBefore": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blacklistDetails.countAfter` | number | Blacklist count after deleting numbers. |
| `blacklistDetails.countBefore` | number | Blacklist count before deleting numbers. |

## Native endpoint

Through the native Sempico Solutions SMS API, this operation is `POST /black-list-delete` (base URL `https://restapi.sempico.solutions/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-blacklist-numbers.md) for the provider-specific parameters and requirements.

