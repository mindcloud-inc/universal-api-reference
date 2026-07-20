# Productify.ai Universal API Examples

These examples use the MindCloud API key and Productify.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Balance



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/get-account-balance?${params}`, {
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
      "creditBalance": 1,
      "extractCostBreakdown": [
        {}
      ],
      "generateCostBreakdown": [
        {}
      ],
      "responseMessage": "string",
      "transformCostBreakdown": [
        {}
      ],
      "wasSuccessful": true
    }
  ],
  "meta": {}
}
```

See the full [Get Account Balance action reference](actions/get-account-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/productifyai/latest/actions/get-account-balance).

## Create Digitisation Batch



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/create-digitisation-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "extractInputs[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/create-digitisation-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "extractInputs[]": [{}]
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
      "batchId": 1,
      "batchSizeLimitExceeded": true,
      "creditCost": 1,
      "creditLimitReached": true,
      "creditsRemaining": 1,
      "currentBalance": 1,
      "responseMessage": "string",
      "validationResults": [
        {}
      ],
      "validations": [
        {}
      ],
      "wasSuccessful": true
    }
  ],
  "meta": {}
}
```

See the full [Create Digitisation Batch action reference](actions/create-digitisation-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/productifyai/latest/actions/create-digitisation-batch).
