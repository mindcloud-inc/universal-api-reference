# TaxBandits: Request WH Certificate by Email

Creates a withholding certificate request by email in TaxBandits.

```
POST https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/request-wh-certificate-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaxBandits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/request-wh-certificate-by-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/request-wh-certificate-by-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "Errors": [
        {}
      ],
      "Requester": {},
      "SubmissionId": "string",
      "WhCertificate": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<object> |  |
| `Requester` | object |  |
| `SubmissionId` | string |  |
| `WhCertificate` | object |  |

## Native endpoint

Through the native TaxBandits API, this operation is `POST WhCertificate/RequestByEmail` (base URL `https://testapi.taxbandits.com/v1.7.3/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-wh-certificate-by-email.md) for the provider-specific parameters and requirements.

