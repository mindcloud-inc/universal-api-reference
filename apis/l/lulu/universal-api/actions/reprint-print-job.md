# Lulu: Reprint Print Job

Creates a reprint of a print job in Lulu.

```
POST https://connect.mindcloud.co/v1/universal/lulu/latest/actions/reprint-print-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lulu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/reprint-print-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactEmail": "apps@mindcloud.co",
  "lineItems[]": [
    {
      "cover": {
        "source_url": "https://www.dropbox.com/sh/p3zh22vzsaegiri/AADP367j0bTWlt8fCu-_tm2ia/161025/139056_cover.pdf?dl=1"
      },
      "title": "MindCloud Test Book",
      "interior": {
        "source_url": "https://www.dropbox.com/sh/p3zh22vzsaegiri/AACOUn3LFKsITDzylh13bQpsa/161025/thesis2.pdf?dl=1"
      },
      "quantity": 1,
      "page_count": 32,
      "external_id": "mc-lulu-reprint-test-1",
      "pod_package_id": "0600X0900.BW.STD.PB.060UW444.MXX"
    }
  ],
  "shippingAddress": {
    "city": "Washington",
    "name": "MindCloud QA",
    "street1": "101 Independence Ave SE",
    "postcode": "20540",
    "state_code": "DC",
    "country_code": "US",
    "phone_number": "+12025550123"
  },
  "shippingLevel": "MAIL"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lulu/latest/actions/reprint-print-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactEmail": "apps@mindcloud.co",
    "lineItems[]": [{"cover":{"source_url":"https://www.dropbox.com/sh/p3zh22vzsaegiri/AADP367j0bTWlt8fCu-_tm2ia/161025/139056_cover.pdf?dl=1"},"title":"MindCloud Test Book","interior":{"source_url":"https://www.dropbox.com/sh/p3zh22vzsaegiri/AACOUn3LFKsITDzylh13bQpsa/161025/thesis2.pdf?dl=1"},"quantity":1,"page_count":32,"external_id":"mc-lulu-reprint-test-1","pod_package_id":"0600X0900.BW.STD.PB.060UW444.MXX"}],
    "shippingAddress": {"city":"Washington","name":"MindCloud QA","street1":"101 Independence Ave SE","postcode":"20540","state_code":"DC","country_code":"US","phone_number":"+12025550123"},
    "shippingLevel": "MAIL"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactEmail` | string | yes | Email contact for the Lulu reprint job. Default: `apps@mindcloud.co`. |
| `lineItems[]` | array | yes | Array of Lulu reprint line items. Default: `[{"cover":{"source_url":"https://www.dropbox.com/sh/p3zh22vzsaegiri/AADP367j0bTWlt8fCu-_tm2ia/161025/139056_cover.pdf?dl=1"},"title":"MindCloud Test Book","interior":{"source_url":"https://www.dropbox.com/sh/p3zh22vzsaegiri/AACOUn3LFKsITDzylh13bQpsa/161025/thesis2.pdf?dl=1"},"quantity":1,"page_count":32,"external_id":"mc-lulu-reprint-test-1","pod_package_id":"0600X0900.BW.STD.PB.060UW444.MXX"}]`. |
| `shippingAddress` | object | yes | Shipping address for the Lulu reprint job. Default: `{"city":"Washington","name":"MindCloud QA","street1":"101 Independence Ave SE","postcode":"20540","state_code":"DC","country_code":"US","phone_number":"+12025550123"}`. |
| `shippingLevel` | string | yes | Shipping level for the Lulu reprint job. Default: `MAIL`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactEmail": "ava@example.com",
      "costs": {},
      "estimatedShippingDates": {
        "arrivalMax": "string",
        "arrivalMin": "string"
      },
      "externalId": "string",
      "id": 1,
      "lineItems": [
        [
          {}
        ]
      ],
      "shippingLevel": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactEmail` | string |  |
| `costs` | object |  |
| `estimatedShippingDates` | object |  |
| `estimatedShippingDates.arrivalMax` | string |  |
| `estimatedShippingDates.arrivalMin` | string |  |
| `externalId` | string |  |
| `id` | number |  |
| `lineItems[]` | array<object> |  |
| `lineItems[].externalId` | string |  |
| `shippingLevel` | string |  |

## Native endpoint

Through the native Lulu API, this operation is `POST /print-jobs/` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reprint-print-job.md) for the provider-specific parameters and requirements.

