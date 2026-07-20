# BlueSnap: Retrieve Vaulted Shopper

Retrieves a vaulted shopper from BlueSnap.

```
GET https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/retrieve-vaulted-shopper
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueSnap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/retrieve-vaulted-shopper?connectionId=$CONNECTION_ID&vaultedShopperId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vaultedShopperId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/retrieve-vaulted-shopper?${params}`, {
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
| `vaultedShopperId` | string | yes | BlueSnap vaulted shopper identifier to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "dateCreated": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "shopperCurrency": "string",
      "timeCreated": "string",
      "vaultedShopperId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string | Country code. |
| `dateCreated` | string | Creation date. |
| `email` | string | Email address. |
| `firstName` | string | First name. |
| `lastName` | string | Last name. |
| `shopperCurrency` | string | Shopper currency. |
| `timeCreated` | string | Creation time. |
| `vaultedShopperId` | number | Vaulted shopper ID. |

## Native endpoint

Through the native BlueSnap API, this operation is `GET /vaulted-shoppers/:vaultedShopperId` (base URL `https://sandbox.bluesnap.com/services/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-vaulted-shopper.md) for the provider-specific parameters and requirements.

