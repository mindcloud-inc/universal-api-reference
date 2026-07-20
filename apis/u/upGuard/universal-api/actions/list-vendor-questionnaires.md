# UpGuard: List Vendor Questionnaires

Retrieves vendor questionnaires from your UpGuard account.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-vendor-questionnaires
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-vendor-questionnaires?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-vendor-questionnaires?${params}`, {
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
| `excludeArchived` | string | no | Exclude archived questionnaires from the results. |
| `usageType` | string | no | The usage type of questionnaires to return. |
| `vendorId` | string | no | The ID of the vendor whose questionnaires should be listed. |
| `vendorPrimaryHostname` | string | no | The primary hostname of the vendor whose questionnaires should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sharedQuestionnaires": [
        {
          "id": 1,
          "includedInRiskProfile": true,
          "inRemediation": true,
          "name": "Ava Chen",
          "publishedAt": "string"
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
| `sharedQuestionnaires[].id` | number |  |
| `sharedQuestionnaires[].includedInRiskProfile` | boolean |  |
| `sharedQuestionnaires[].inRemediation` | boolean |  |
| `sharedQuestionnaires[].name` | string |  |
| `sharedQuestionnaires[].publishedAt` | string |  |

## Native endpoint

Through the native UpGuard API, this operation is `GET /vendor/questionnaires/v2` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vendor-questionnaires.md) for the provider-specific parameters and requirements.

