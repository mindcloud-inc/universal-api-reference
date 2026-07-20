# Smarty-streets: Lookup International Postal Code

Retrieves international postal code details from Smarty-streets by postal code.

```
GET https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/lookup-international-postal-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smarty-streets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/lookup-international-postal-code?connectionId=$CONNECTION_ID&country=CAN&postalCode=T4B%205M7" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "CAN",
  "postalCode": "T4B 5M7"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/lookup-international-postal-code?${params}`, {
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
| `country` | string | yes | Country name or ISO country code. Default: `CAN`. Example: `CAN`. |
| `postalCode` | string | yes | Postal code to look up. Default: `T4B 5M7`. Example: `T4B 5M7`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Smarty-streets API returns.

## Native endpoint

Through the native Smarty-streets API, this operation is `GET https://international-postal-code.api.smarty.com/lookup` (base URL `https://us-street.api.smarty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-international-postal-code.md) for the provider-specific parameters and requirements.

