# condoo: Delete Custom Domain

Deletes an existing custom domain from condoo.

```
DELETE https://connect.mindcloud.co/v1/universal/condoo/latest/actions/delete-custom-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/delete-custom-domain?connectionId=$CONNECTION_ID&domainId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/condoo/latest/actions/delete-custom-domain?${params}`, {
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
| `domainId` | number | yes | Required custom domain ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native condoo API, this operation is `DELETE /domains/{domain_id}` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-custom-domain.md) for the provider-specific parameters and requirements.

