# TPS API: Screen Phone Numbers

Screens phone numbers against TPS and CTPS lists in TPS API.

```
GET https://connect.mindcloud.co/v1/universal/tPSAPI/latest/actions/screen-phone-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TPS API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tPSAPI/latest/actions/screen-phone-numbers?connectionId=$CONNECTION_ID&phoneNumbers=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phoneNumbers": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tPSAPI/latest/actions/screen-phone-numbers?${params}`, {
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
| `phoneNumbers` | list<string> | yes | Phone numbers to screen against the selected TPS lists. |
| `checkTps` | boolean | no | Screen numbers against the TPS list. Default: `true`. |
| `checkCtps` | boolean | no | Screen numbers against the CTPS list. Default: `false`. |
| `returnCallableNumbersOnly` | boolean | no | Return only numbers that are not on the selected list or lists. Default: `false`. |
| `returnPrettierNumbers` | boolean | no | Include a prettier phone number field in the response. Default: `false`. |
| `returnDateAdded` | boolean | no | Include the date each number was added to the selected list or lists. Default: `false`. |
| `noLogging` | boolean | no | Prevent the provider from storing full numbers in logs. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TPS API API returns.

## Native endpoint

Through the native TPS API API, this operation is `POST /` (base URL `https://service.tpsapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/screen-phone-numbers.md) for the provider-specific parameters and requirements.

