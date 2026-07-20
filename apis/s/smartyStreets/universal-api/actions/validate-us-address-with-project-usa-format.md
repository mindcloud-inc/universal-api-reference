# Smarty-streets: Validate US Address With Project USA Format

Retrieves a validated US address from Smarty-streets in Project USA format.

```
GET https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/validate-us-address-with-project-usa-format
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smarty-streets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/validate-us-address-with-project-usa-format?connectionId=$CONNECTION_ID&street=1%20Santa%20Claus%20Ln%2C%20North%20Pole%2C%20AK" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "street": "1 Santa Claus Ln, North Pole, AK"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/validate-us-address-with-project-usa-format?${params}`, {
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
| `street` | string | yes | Address text to verify. Default: `1 Santa Claus Ln, North Pole, AK`. Example: `1 Santa Claus Ln, North Pole, AK`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Smarty-streets API returns.

## Native endpoint

Through the native Smarty-streets API, this operation is `GET https://us-street.api.smarty.com/street-address` (base URL `https://us-street.api.smarty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-us-address-with-project-usa-format.md) for the provider-specific parameters and requirements.

