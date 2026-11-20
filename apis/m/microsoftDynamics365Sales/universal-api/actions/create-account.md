# Microsoft Dynamics 365 Sales: Create Account



```
POST https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/create-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 Sales `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fields": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fields": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recordId` | string | no | Optional deterministic GUID. Sent as accountid in the POST body; omit to let Dataverse assign an ID. |
| `fields` | object | yes | Required writable Dataverse columns by logical name, including grny_aspireid. Do not repeat accountid inside Fields; use Record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountid` | string | GUID of the created Dynamics record, returned by Prefer: return=representation. |

## Native endpoint

Through the native Microsoft Dynamics 365 Sales API, this operation is `POST /accounts` (base URL `{{credentials.environmentUrl}}/api/data/v9.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-account.md) for the provider-specific parameters and requirements.

