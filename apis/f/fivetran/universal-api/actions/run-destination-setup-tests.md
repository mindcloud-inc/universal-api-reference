# Fivetran: Run Destination Setup Tests

Runs setup tests for a destination in Fivetran.

```
PUT https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/run-destination-setup-tests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fivetran `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/run-destination-setup-tests" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destinationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/run-destination-setup-tests', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destinationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `destinationId` | string | yes | The unique identifier for the destination within Fivetran. |
| `trustCertificates` | boolean | no | Trust certificates automatically during destination setup tests. |
| `trustFingerprints` | boolean | no | Trust SSH fingerprints automatically during destination setup tests. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "setupTests": {},
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `setupTests` | object |  |
| `status` | object |  |

## Native endpoint

Through the native Fivetran API, this operation is `POST /destinations/[:destinationId]/test` (base URL `https://api.fivetran.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-destination-setup-tests.md) for the provider-specific parameters and requirements.

