# Global Patron: List Accessible Forms

Lists accessible forms in Global Patron.

```
GET https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-accessible-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Patron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-accessible-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-accessible-forms?${params}`, {
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
      "accessibleFormIdsAccountManagementAccess": [
        "string"
      ],
      "accessibleFormIdsEditAccess": [
        "string"
      ],
      "accessibleFormIdsFullReportingAccess": [
        "string"
      ],
      "results": [
        {
          "createdDateUtc": "2026-05-07T12:00:00.000Z",
          "formConfiguration": {
            "settings": {
              "formDescription": "string",
              "formName": "Ava Chen",
              "formSystemVersion": 1,
              "formType": "string"
            }
          },
          "id": "string",
          "modifiedDateUtc": "2026-05-07T12:00:00.000Z"
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
| `accessibleFormIdsAccountManagementAccess` | array<string> | Form ids with account-management access. |
| `accessibleFormIdsEditAccess` | array<string> | Form ids with edit access. |
| `accessibleFormIdsFullReportingAccess` | array<string> | Form ids with full reporting access. |
| `results` | array<object> | Forms available to the current account. |
| `results[].createdDateUtc` | date | Creation timestamp. |
| `results[].formConfiguration` | object | Basic form configuration. |
| `results[].formConfiguration.settings` | object | Basic form settings. |
| `results[].formConfiguration.settings.formDescription` | string | Form description. |
| `results[].formConfiguration.settings.formName` | string | Form name. |
| `results[].formConfiguration.settings.formSystemVersion` | number | Form system version. |
| `results[].formConfiguration.settings.formType` | string | Form type. |
| `results[].id` | string | Form identifier. |
| `results[].modifiedDateUtc` | date | Last modification timestamp. |

## Native endpoint

Through the native Global Patron API, this operation is `GET /api/restricted/user/form` (base URL `https://api.globalpatron.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-accessible-forms.md) for the provider-specific parameters and requirements.

