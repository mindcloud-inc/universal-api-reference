# Global Patron: List Accessible Datalists

Lists accessible datalists in Global Patron.

```
GET https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-accessible-datalists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Patron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-accessible-datalists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-accessible-datalists?${params}`, {
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
      "accessibleDatalistIdsAccountManagementAccess": [
        "string"
      ],
      "accessibleDatalistIdsEditAccess": [
        "string"
      ],
      "accessibleDatalistIdsFullReportingAccess": [
        "string"
      ],
      "results": [
        {
          "createdDateUtc": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "modifiedDateUtc": "2026-05-07T12:00:00.000Z",
          "settings": {
            "listDescription": "string",
            "listName": "Ava Chen",
            "listType": "string"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessibleDatalistIdsAccountManagementAccess` | array<string> | Datalist ids with account-management access. |
| `accessibleDatalistIdsEditAccess` | array<string> | Datalist ids with edit access. |
| `accessibleDatalistIdsFullReportingAccess` | array<string> | Datalist ids with full reporting access. |
| `results` | array<object> | Datalists available to the current account. |
| `results[].createdDateUtc` | date | Creation timestamp. |
| `results[].id` | string | Datalist identifier. |
| `results[].modifiedDateUtc` | date | Last modification timestamp. |
| `results[].settings` | object | Datalist settings. |
| `results[].settings.listDescription` | string | Datalist description. |
| `results[].settings.listName` | string | Datalist name. |
| `results[].settings.listType` | string | Datalist type. |

## Native endpoint

Through the native Global Patron API, this operation is `GET /api/restricted/user/datalist` (base URL `https://api.globalpatron.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-accessible-datalists.md) for the provider-specific parameters and requirements.

