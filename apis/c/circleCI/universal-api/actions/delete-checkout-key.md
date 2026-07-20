# CircleCI: Delete Checkout Key



```
DELETE https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/delete-checkout-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/delete-checkout-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/delete-checkout-key?${params}`, {
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
| `fingerprint` | string | no | Checkout key fingerprint. |
| `projectSlug` | string | no | Project slug in the form vcs/org/repo. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fingerprint": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fingerprint` | string |  |
| `message` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `DELETE /project/:project_slug/checkout-key/:fingerprint` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-checkout-key.md) for the provider-specific parameters and requirements.

