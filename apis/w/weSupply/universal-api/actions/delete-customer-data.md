# WeSupply: Delete Customer Data

Deletes customer data from WeSupply.

```
DELETE https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/delete-customer-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeSupply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/delete-customer-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/delete-customer-data?${params}`, {
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
| `customerEmail` | string | no | The customer email address whose data should be deleted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sucess": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sucess` | boolean | Documented WeSupply success flag returned by the GDPR delete endpoint. |

## Native endpoint

Through the native WeSupply API, this operation is `POST /gdpr/delete` (base URL `https://{{credentials.subdomain}}.labs.wesupply.xyz/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-customer-data.md) for the provider-specific parameters and requirements.

