# Sendible: Disable Feature Tag



```
DELETE https://connect.mindcloud.co/v1/universal/sendible/latest/actions/disable-feature-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendible `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sendible/latest/actions/disable-feature-tag?connectionId=$CONNECTION_ID&featureTagId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "featureTagId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendible/latest/actions/disable-feature-tag?${params}`, {
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
| `featureTagId` | number | yes | Feature tag ID to disable. |
| `target` | string | no | Feature target scope. Default: `user`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enabled": true,
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | boolean |  |
| `id` | number |  |

## Native endpoint

Through the native Sendible API, this operation is `DELETE api/v2/features` (base URL `https://api.sendible.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/disable-feature-tag.md) for the provider-specific parameters and requirements.

