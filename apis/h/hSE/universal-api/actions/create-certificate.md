# 4HSE: Create Certificate

Creates a new certificate in 4HSE.

```
POST https://connect.mindcloud.co/v1/universal/hSE/latest/actions/create-certificate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/create-certificate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dateRelease": "2026-05-07T12:00:00.000Z",
  "name": "Ava Chen",
  "actionType": "0",
  "resourceId": "string",
  "tenantId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hSE/latest/actions/create-certificate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dateRelease": "2026-05-07T12:00:00.000Z",
    "name": "Ava Chen",
    "actionType": "0",
    "resourceId": "string",
    "tenantId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dateRelease` | date | yes | Issue date of the certificate. |
| `dateExpire` | date | no | Expiration date of the certificate. |
| `name` | string | yes | Descriptive name of the certificate. |
| `actionType` | string | yes | The type of requirement this certificate relates to. One of: `0`, `1`, `2`, `3`, `4`. |
| `resourceId` | string | yes | The resource this certificate is issued to. |
| `tenantId` | string | yes | The project this certificate belongs to. |
| `validityUnit` | string | no | Unit for the certificate validity period. One of: `0`, `1`, `2`. |
| `validity` | number | no | Number of validity units. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `note` | string | no | Free-text notes. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 4HSE API returns.

## Native endpoint

Through the native 4HSE API, this operation is `POST /v2/certificate/create` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-certificate.md) for the provider-specific parameters and requirements.

