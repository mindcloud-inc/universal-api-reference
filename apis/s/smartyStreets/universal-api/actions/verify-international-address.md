# Smarty-streets: Verify International Address

Retrieves international address verification details from Smarty-streets.

```
GET https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/verify-international-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smarty-streets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/verify-international-address?connectionId=$CONNECTION_ID&country=Brazil&freeform=Rua%20Padre%20Antonio%20D'Angelo%20121%20Sao%20Paulo%2002516-040%20SP" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "Brazil",
  "freeform": "Rua Padre Antonio D'Angelo 121 Sao Paulo 02516-040 SP"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/verify-international-address?${params}`, {
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
| `country` | string | yes | Country name or ISO country code. Default: `Brazil`. Example: `Brazil`. |
| `freeform` | string | yes | Entire address minus the country. Default: `Rua Padre Antonio D'Angelo 121 Sao Paulo 02516-040 SP`. Example: `Rua Padre Antonio D'Angelo 121 Sao Paulo 02516-040 SP`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Smarty-streets API returns.

## Native endpoint

Through the native Smarty-streets API, this operation is `GET https://international-street.api.smarty.com/verify` (base URL `https://us-street.api.smarty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-international-address.md) for the provider-specific parameters and requirements.

