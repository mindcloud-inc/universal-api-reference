# Recommand: Create Company Identifier

Creates a new company identifier in Recommand.

```
POST https://connect.mindcloud.co/v1/universal/recommand/latest/actions/create-company-identifier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/create-company-identifier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyid": "string",
  "identifier": "string",
  "scheme": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recommand/latest/actions/create-company-identifier', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyid": "string",
    "identifier": "string",
    "scheme": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyid` | string | yes | companyId parameter. |
| `identifier` | string | yes | The value of the identifier |
| `scheme` | string | yes | The scheme of the identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "identifier": {
        "companyId": "string",
        "createdAt": "string",
        "id": "string",
        "identifier": "string",
        "scheme": "string",
        "updatedAt": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `identifier` | object |  |
| `identifier.companyId` | string |  |
| `identifier.createdAt` | string |  |
| `identifier.id` | string |  |
| `identifier.identifier` | string |  |
| `identifier.scheme` | string |  |
| `identifier.updatedAt` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Recommand API, this operation is `POST /api/v1/companies/:companyId/identifiers` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company-identifier.md) for the provider-specific parameters and requirements.

