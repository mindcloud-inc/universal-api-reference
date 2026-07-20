# Recommand: Get Company Identifier

Retrieves a company identifier from Recommand.

```
GET https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-company-identifier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-company-identifier?connectionId=$CONNECTION_ID&companyid=string&identifierid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyid": "string",
  "identifierid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-company-identifier?${params}`, {
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
| `companyid` | string | yes | companyId parameter. |
| `identifierid` | string | yes | identifierId parameter. |

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

Through the native Recommand API, this operation is `GET /api/v1/companies/:companyId/identifiers/:identifierId` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-identifier.md) for the provider-specific parameters and requirements.

