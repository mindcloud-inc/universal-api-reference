# Better Proposals: Get Settings

Retrieves account settings from Better Proposals.

```
GET https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Proposals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-settings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accountID": "string",
      "currencyID": "string",
      "customerJourneysActive": "string",
      "customerJourneysDefault": "string",
      "dateEdited": "2026-05-07T12:00:00.000Z",
      "editedBy": {},
      "id": "string",
      "tax": "string",
      "taxAmount": {},
      "taxLabel": {},
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountID` | string |  |
| `currencyID` | string |  |
| `customerJourneysActive` | string |  |
| `customerJourneysDefault` | string |  |
| `dateEdited` | date |  |
| `editedBy` | object |  |
| `id` | string |  |
| `tax` | string |  |
| `taxAmount` | object |  |
| `taxLabel` | object |  |
| `timeZone` | string |  |

## Native endpoint

Through the native Better Proposals API, this operation is `GET /settings` (base URL `https://api.betterproposals.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-settings.md) for the provider-specific parameters and requirements.

