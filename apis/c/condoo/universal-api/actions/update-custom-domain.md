# condoo: Update Custom Domain

Updates an existing custom domain in condoo.

```
PUT https://connect.mindcloud.co/v1/universal/condoo/latest/actions/update-custom-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/update-custom-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domainId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/condoo/latest/actions/update-custom-domain', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domainId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customIndexUrl` | string | no | Optional custom index URL. |
| `customNotFoundUrl` | string | no | Optional custom not-found URL. |
| `domainId` | number | yes | Required custom domain ID. |
| `host` | string | no | Optional custom domain host. |

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

Through the native condoo API, this operation is `POST /domains/{domain_id}` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-custom-domain.md) for the provider-specific parameters and requirements.

