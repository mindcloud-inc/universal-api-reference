# Better Proposals: Get Brand Settings

Retrieves brand settings from Better Proposals.

```
GET https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-brand-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Proposals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-brand-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-brand-settings?${params}`, {
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
      "companyName": "Ava Chen",
      "createdBy": "string",
      "currencyID": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateEdited": "2026-05-07T12:00:00.000Z",
      "default": "string",
      "deleted": "string",
      "editedBy": {},
      "id": "string",
      "name": "Ava Chen",
      "pageTitle": {},
      "showBadge": "string",
      "tax": "string",
      "taxAmount": {},
      "taxLabel": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountID` | string |  |
| `companyName` | string |  |
| `createdBy` | string |  |
| `currencyID` | string |  |
| `dateCreated` | date |  |
| `dateEdited` | date |  |
| `default` | string |  |
| `deleted` | string |  |
| `editedBy` | object |  |
| `id` | string |  |
| `name` | string |  |
| `pageTitle` | object |  |
| `showBadge` | string |  |
| `tax` | string |  |
| `taxAmount` | object |  |
| `taxLabel` | object |  |

## Native endpoint

Through the native Better Proposals API, this operation is `GET /settings/brand` (base URL `https://api.betterproposals.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-brand-settings.md) for the provider-specific parameters and requirements.

