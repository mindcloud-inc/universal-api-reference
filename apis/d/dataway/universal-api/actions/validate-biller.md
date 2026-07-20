# Dataway: Validate Biller

Validates a biller in Dataway for a selected service.

```
GET https://connect.mindcloud.co/v1/universal/dataway/latest/actions/validate-biller
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dataway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataway/latest/actions/validate-biller?connectionId=$CONNECTION_ID&service_slug=string&biller_identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "service_slug": "string",
  "biller_identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataway/latest/actions/validate-biller?${params}`, {
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
| `service_slug` | string | yes | Vendor service slug to validate against. |
| `biller_identifier` | string | yes | Customer identifier such as phone number or meter number. |
| `variation_slug` | string | no | Optional variation slug when the service requires a variation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "billerIdentifier": "string",
        "customerName": "Ava Chen",
        "serviceSlug": "string",
        "variationSlug": "string"
      },
      "responseCode": "string",
      "responseDescription": "string",
      "responseMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Validated biller payload returned by the provider. |
| `data.billerIdentifier` | string | Validated identifier echoed by the provider. |
| `data.customerName` | string | Validated customer name when returned. |
| `data.serviceSlug` | string | Validated service slug when returned. |
| `data.variationSlug` | string | Validated variation slug when returned. |
| `responseCode` | string | Provider response code. |
| `responseDescription` | string | Provider response description. |
| `responseMessage` | string | Provider response message. |

## Native endpoint

Through the native Dataway API, this operation is `POST /validate-biller` (base URL `https://datawayapp.com/vendor`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-biller.md) for the provider-specific parameters and requirements.

