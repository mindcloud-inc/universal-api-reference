# PhantomBuster: Compare Branches

Retrieves differences between branches in PhantomBuster.

```
GET https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/compare-branches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhantomBuster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/compare-branches?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/compare-branches?${params}`, {
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
| `name` | string | yes | Name of the script branch to fetch the diff from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "diffLength": 1,
      "id": "string",
      "name": "Ava Chen",
      "releaseVisibility": "string",
      "stagingVisibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `diffLength` | number |  |
| `id` | string |  |
| `name` | string |  |
| `releaseVisibility` | string |  |
| `stagingVisibility` | string |  |

## Native endpoint

Through the native PhantomBuster API, this operation is `GET /branches/diff` (base URL `https://api.phantombuster.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compare-branches.md) for the provider-specific parameters and requirements.

