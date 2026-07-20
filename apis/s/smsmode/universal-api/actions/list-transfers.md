# smsmode: List Transfers



```
GET https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/list-transfers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smsmode `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/list-transfers?connectionId=$CONNECTION_ID&limit=25&offset=0&organisationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organisationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/list-transfers?${params}`, {
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
| `organisationId` | string | yes | Organisation ID path parameter from the smsmode API route. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "creationDate": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "description": "string",
      "href": "string",
      "organisationDestination": {
        "name": "Ava Chen",
        "organisationId": "string"
      },
      "organisationSource": {
        "name": "Ava Chen",
        "organisationId": "string"
      },
      "reference": "string",
      "transferId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `creationDate` | date |  |
| `currency` | string |  |
| `description` | string |  |
| `href` | string |  |
| `organisationDestination.name` | string |  |
| `organisationDestination.organisationId` | string |  |
| `organisationSource.name` | string |  |
| `organisationSource.organisationId` | string |  |
| `reference` | string |  |
| `transferId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native smsmode API, this operation is `GET commons/v1/organisations/:organisationId/transfers` (base URL `https://rest.smsmode.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transfers.md) for the provider-specific parameters and requirements.

