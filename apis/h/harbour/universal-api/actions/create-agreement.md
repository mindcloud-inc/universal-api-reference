# Harbour: Create Agreement

Creates a new agreement in Harbour.

```
POST https://connect.mindcloud.co/v1/universal/harbour/latest/actions/create-agreement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harbour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/harbour/latest/actions/create-agreement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file_upload": {},
  "agreement_data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harbour/latest/actions/create-agreement', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file_upload": {},
    "agreement_data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file_upload` | object | yes | Object with name and base64 for the agreement file. |
| `agreement_data` | object | yes | Agreement metadata, inputs, and template settings. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agreement": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agreement` | object |  |

## Native endpoint

Through the native Harbour API, this operation is `POST https://api.harbourshare.com/v1/agreements` (base URL `https://api.myharbourshare.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agreement.md) for the provider-specific parameters and requirements.

