# DigiCert: List Subaccount Domains

Retrieves domain details from a DigiCert subaccount.

```
GET https://connect.mindcloud.co/v1/universal/digiCert/latest/actions/list-subaccount-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DigiCert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiCert/latest/actions/list-subaccount-domains?connectionId=$CONNECTION_ID&subaccountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subaccountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiCert/latest/actions/list-subaccount-domains?${params}`, {
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
| `subaccountId` | string | yes | The DigiCert subaccount identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native DigiCert API, this operation is `GET /account/subaccount/:subaccount_id/domain` (base URL `https://www.digicert.com/services/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subaccount-domains.md) for the provider-specific parameters and requirements.

