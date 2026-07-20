# Lulu Universal API Examples

These examples use the MindCloud API key and Lulu connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Print Jobs

Retrieves print jobs from Lulu.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/list-print-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lulu/latest/actions/list-print-jobs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Print Jobs action reference](actions/list-print-jobs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lulu/latest/actions/list-print-jobs).

## Create Print Job

Creates a new print job in Lulu.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/create-print-job" \
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
      "external_id": "mc-lulu-test-1",
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/lulu/latest/actions/create-print-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactEmail": "apps@mindcloud.co",
    "lineItems[]": [{"cover":{"source_url":"https://www.dropbox.com/sh/p3zh22vzsaegiri/AADP367j0bTWlt8fCu-_tm2ia/161025/139056_cover.pdf?dl=1"},"title":"MindCloud Test Book","interior":{"source_url":"https://www.dropbox.com/sh/p3zh22vzsaegiri/AACOUn3LFKsITDzylh13bQpsa/161025/thesis2.pdf?dl=1"},"quantity":1,"page_count":32,"external_id":"mc-lulu-test-1","pod_package_id":"0600X0900.BW.STD.PB.060UW444.MXX"}],
    "shippingAddress": {"city":"Washington","name":"MindCloud QA","street1":"101 Independence Ave SE","postcode":"20540","state_code":"DC","country_code":"US","phone_number":"+12025550123"},
    "shippingLevel": "MAIL"
  })
});

const { success, data } = await response.json();
```

Example response:

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

See the full [Create Print Job action reference](actions/create-print-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lulu/latest/actions/create-print-job).
