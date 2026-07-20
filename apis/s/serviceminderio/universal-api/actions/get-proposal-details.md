# serviceminder.io: Get Proposal Details

Retrieves proposal details from ServiceMinder.

```
GET https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/get-proposal-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a serviceminder.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/get-proposal-details?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/get-proposal-details?${params}`, {
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
| `id` | number | yes | Proposal identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bundledProposals": [
        {}
      ],
      "changeOrders": [
        {}
      ],
      "contactId": 1,
      "customFields": [
        {}
      ],
      "id": 1,
      "message": "string",
      "proposalLines": [
        {}
      ],
      "proposalNotes": [
        {}
      ],
      "resultCode": 1,
      "serviceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bundledProposals` | array<object> |  |
| `changeOrders` | array<object> |  |
| `contactId` | number |  |
| `customFields` | array<object> |  |
| `id` | number |  |
| `message` | string |  |
| `proposalLines` | array<object> |  |
| `proposalNotes` | array<object> |  |
| `resultCode` | number |  |
| `serviceId` | number |  |

## Native endpoint

Through the native serviceminder.io API, this operation is `POST /proposal/details` (base URL `https://serviceminder.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-proposal-details.md) for the provider-specific parameters and requirements.

